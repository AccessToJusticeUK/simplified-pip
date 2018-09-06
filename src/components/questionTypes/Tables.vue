<template>
    <div class="question table">
        <span class="check">✔</span>
        
        <table>
            <thead>
                <tr>
                    <th v-for="col in columns">{{col.title}}</th>
                    <th></th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="(row, index) in rows">
                    <td v-for="col in columns">
                        <textarea
                            v-model="col.value" 
                            :style="{width: col.widthPx + 'px'}"
                            :placeholder="col.placeholder"></textarea>
                    </td>
                    <td class="action-button">
                        <button @click="addRow()" v-if="index > 0" class="table-delete-button">➖</button>
                    </td>
                </tr>
                
            </tbody>
        </table>

        <button @click="addRow()" class="table-add-button">➕</button>
    </div>
</template>

<style scoped lang="scss">
</style>
<script>
export default {
  name: "Table",
  props: {
    columns: Array
  },
  methods: {
      addRow: function () {
          this.rows.push({});
      }
  },
  data: function () {
      return {
          rows: [{}]
      }
  }
}
</script>
