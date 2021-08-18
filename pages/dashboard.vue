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
            <span>{{ dataItem.amount }}</span>
            <span class="table-tag">
              <span>{{ dataItem.status }} </span>
              <span>
                <svg
                  width="16"
                  height="16"
                  viewBox="0 0 16 16"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    fill-rule="evenodd"
                    clip-rule="evenodd"
                    d="M5.97274 11.9097L2.21974 8.19125C1.92724 7.89575 1.92724 7.4165 2.21974 7.12175C2.51224 6.827 2.98774 6.82625 3.28024 7.12175L6.50074 10.2897L12.7167 4.09625C13.0092 3.8015 13.4847 3.8015 13.7772 4.09625C14.0697 4.391 14.0697 4.871 13.7772 5.16575L7.02499 11.906C6.88579 12.0455 6.69705 12.1241 6.50001 12.1248C6.30298 12.1255 6.11368 12.0482 5.97349 11.9097H5.97274Z"
                    fill="#0E6245"
                  />
                </svg>
              </span>
            </span>
          </template>
        </Table>
      </main>
    </div>
  </div>
</template>
<script>
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
}
</script>
