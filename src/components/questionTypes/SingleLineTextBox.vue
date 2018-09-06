<template>
    <div class="question single-line">
        <span class="check"></span>
        <input placeholder="{{placeholder}}" type="text" />
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
          
      }
  }
};
</script>