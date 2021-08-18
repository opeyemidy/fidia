<template>
  <div>
    <div class="table-container">
      <table>
        <thead>
          <tr>
            <th><input id="" type="checkbox" name="" /></th>
            <th v-for="header in headers" :key="header.value">
              {{ header.text }}
            </th>
            <th></th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="item in items" :key="item[itemKey]">
            <td><input id="" type="checkbox" name="" /></td>
            <td v-for="dataItem in headers" :key="dataItem.value">
              <slot :name="dataItem.value" :data-item="item">{{
                item[dataItem.value]
              }}</slot>
            </td>
            <td>...</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="d-flex table-footer justify-content-between">
      <span>{{ items.length }} results</span>
      <div>
        <button class="button btn-disabled">Previous</button>
        <Button> Next </Button>
      </div>
    </div>
  </div>
</template>

<script>
import Button from './Button.vue'
export default {
  components: { Button },
  props: {
    headers: {
      type: Array,
      default: () => {
        return []
      },
    },
    items: {
      type: Array,
      default: () => {
        return []
      },
    },
    itemKey: {
      type: String,
      default: () => {
        return ''
      },
    },
  },
}
</script>
