<template>
  <b-table
    :data="stat.data"
    :columns="stat.columns"
    :default-sort="stat.columns[0].field"
  ></b-table>
</template>

<script>
export default {
  name: 'Stats',
  props: {
    stat: {
      type: Object,
      required: true
    }
  }
}
</script>
