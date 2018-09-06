<template>
    <div class="question single-line">
        <span class="check" v-if="text">✔</span>
        <input :placeholder="placeholder" v-model="text" type="text" />
    </div>
</template>

<style scoped lang="scss">
</style>

<script>
export default {
  name: "Section",
  props: {
    question: {},
    placeholder: ""
  },
  data: function () {
      return {
          text: null
      }
  }
};
</script>