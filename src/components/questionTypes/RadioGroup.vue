<template>
    <div class="question radio-group">
        <span class="check" v-if="selectedOption">✔</span>
        
        <div class="options">
            <span class="option" v-for="option in options.items">
                <label>
                    <input :name="options.key" v-model="selectedOption" :value="option.title" type="radio" />
                    &nbsp;
                    {{option.title}}                        
                </label>
            </span>
        </div>
    </div>
</template>

<style scoped lang="scss">
</style>

<script>
export default {
  name: "RadioGroup",
  props: {
    options: Object
  },
  data: function() {
    return {
      selectedOption: null
    };
  }
};
</script>