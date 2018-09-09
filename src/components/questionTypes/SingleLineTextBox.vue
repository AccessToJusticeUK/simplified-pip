<template>
    <div>
        <span class="check" v-if="text">✔</span>
        <label :for="id">{{ label }}</label>
        <input type="text" v-model.lazy="text" :id="id" :name="id"
               :placeholder="placeholder"
               :class="half ? 'half' : ''" />
    </div>
</template>

<script>
export default {
  name: 'SingleLineTextBox',
  props: {
    id: String,
    label: String,
    placeholder: String,
    half: [Boolean, String]
  },
  data: function () {
    return {
      text: null
    }
  }
}
</script>
