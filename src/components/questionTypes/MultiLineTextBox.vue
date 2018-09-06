<template>
    <div class="question multi-line">
        <span class="check" v-if="text">✔</span>
        <textarea :placeholder="placeholder" v-model="text"></textarea>
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