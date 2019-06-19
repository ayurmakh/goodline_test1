<template>
  <div>
    <table>
      <th v-for="header in headers" :key="header">{{ header }}</th>
      <tr v-for="(row, i) in table" :key="i">
        <td v-for="(val, j) in row" :key="j">{{ val }}</td>
      </tr>
    </table>
  </div>
</template>

<script>
import json from '../data.json'

export default {
  name: 'Table',
  data() {
    return {
      headers: ['name', 'id', 'phone','age'],
      table: json
    }
  }
}
</script>

<style scoped lang="scss">
table {
  font-size: 20px;
  width: 700px
}
td {
  text-align: center;
}
</style>
