<template>
    <div class="question table">
        <table>
            <thead>
                <tr>
                    <th v-for="(col, colIndex) in columns" v-bind:key="colIndex">{{col.title}}</th>
                    <th></th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="(row, index) in rows" v-bind:key="index">
                    <td v-for="(col, colIndex) in columns" v-bind:key="colIndex">
                        <textarea
                            v-model="row[colIndex]"
                            :style="{width: col.widthPx + 'px'}"
                            :placeholder="col.placeholder"></textarea>
                    </td>
                    <td class="action-button">
                        <button @click="removeRow(index)" v-if="rows.length > 1" class="table-delete-button">&mdash;</button>
                    </td>
                </tr>

            </tbody>
        </table>

        <button @click="addRow()" class="table-add-button">+ Add a row</button>
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
      this.rows.push({})
    },

    removeRow: function (index) {
      this.rows.splice(index, 1)
    }
  },
  data: function () {
    return {
      rows: [{}]
    }
  }
}
</script>
