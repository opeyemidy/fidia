<template>
  <div class="dashboard-wrapper">
    <Navbar />
    <div class="dashboard-content">
      <Header />
      <main>
        <div class="main-header d-flex justify-content-between">
          <h1 class="title">Payments</h1>
          <div>
            <Button has-icon>
              <template #icon>
                <filter-icon />
              </template>
              Filter
            </Button>
            <Button has-icon>
              <template #icon>
                <export-icon />
              </template>
              Export
            </Button>
            <Button colored has-icon>
              <template #icon>
                <add-icon />
              </template>
              Create payment
            </Button>
          </div>
        </div>
        <div class="tab-container">
          <Button
            v-for="(tab, i) in tabs"
            :key="i"
            tab
            :class="{ 'pl-0': i === 0, active: i === currentIndex }"
            @click="currentIndex = i"
            >{{ tab }}</Button
          >
        </div>
        <Table :headers="headers" :items="tableData">
          <template #amount="{ dataItem }">
            <span class="price-wrapper">{{ dataItem.amount }}</span>
            <span class="table-tag">
              <span>{{ dataItem.status }} </span>
              <span>
                <tick-icon />
              </span>
            </span>
          </template>
        </Table>
      </main>
    </div>
  </div>
</template>
<script>
import dashboardMeta from '~/data/dasboardMeta'
import AddIcon from '~/components/addIcon.vue'
import Button from '~/components/Button.vue'
import ExportIcon from '~/components/exportIcon.vue'
import FilterIcon from '~/components/filterIcon.vue'
import Header from '~/components/Header.vue'
import Navbar from '~/components/Navbar.vue'
import Table from '~/components/Table.vue'
import tableData from '~/data/tableData'
export default {
  components: {
    Button,
    Navbar,
    Header,
    Table,
    FilterIcon,
    ExportIcon,
    AddIcon,
  },
  data() {
    return {
      tabs: ['All', 'Succeeded', 'Refunded', 'Uncaptured'],
      currentIndex: 1,
      headers: [
        { text: 'Amount', value: 'amount' },
        { text: 'Description', value: 'description' },
        { text: 'Customer', value: 'email' },
        { text: 'Date', value: 'date' },
      ],
      tableData,
    }
  },
  head() {
    return {
      title: 'Dashboard - Fidia',
      meta: dashboardMeta,
    }
  },
}
</script>
