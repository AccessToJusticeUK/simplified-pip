<template>
  <header>
    <h3 v-if="title">{{ title }}</h3>
    <small v-if="description">{{ description }}</small>
  </header>
</template>

<script>
export default {
  props: {
    title: String,
    description: String
  }
}
</script>

<style lang="scss" scoped>
  header {
    margin-top: 50px;
  }
</style>
