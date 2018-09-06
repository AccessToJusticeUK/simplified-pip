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
                    <td v-for="(col, colIndex) in columns">
                        <textarea
                            v-model="row[colIndex]"
                            :style="{width: col.widthPx + 'px'}"
                            :placeholder="col.placeholder"></textarea>
                    </td>
                    <td class="action-button">
                        <button @click="removeRow(index)" v-if="rows.length > 1" class="table-delete-button">➖</button>
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
  name: 'Table',
  props: {
    columns: Array
  },
  methods: {
      addRow: function () {
          this.rows.push({});
      },

      removeRow: function (index) {
          this.rows.splice(index, 1);
      }
  },
  data: function () {
      return {
          rows: []
      }
  }
}
</script>
