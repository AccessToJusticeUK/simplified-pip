<template>
  <div>
    <p>
      <strong>{{ 'Q' + number }}&nbsp;</strong>
      <span>{{ text }}</span>
    </p>
    <p>
      <small v-if="description">{{ description }}</small>
    </p>
  </div>
</template>

<script>

export default {
  name: 'Question',
  props: {
    number: String,
    text: String,
    description: String
  }
}
</script>

<style lang="scss" scoped>
  small {
    display: block;
    font-size: 12px;
  }
</style>
