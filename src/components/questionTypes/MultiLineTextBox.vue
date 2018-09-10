<template>
    <div class="form-input">
        <span class="check" v-if="text">✔</span>
        <label v-if="label" :for="id">{{ label }}</label>
        <textarea :id="id" :name="id" :placeholder="placeholder" :rows="rows" v-model.lazy="text"></textarea>
        <aside v-if="this.$slots.default">
          <slot />
        </aside>
    </div>
</template>

<style scoped lang="scss">
</style>

<script>
export default {
  name: 'MultiLineTextBox',
  props: {
    id: String,
    label: String,
    placeholder: String,
    rows: [Number, String]
  },
  data: function () {
    return {
      text: null
    }
  }
}
</script>
