<template>
<!--
  {
    fileName: String,
    preload: Boolean,
    cssClass: String
  }
-->
<div v-if="model.fileName" :class="'help-text ' + model.cssClass">
  <div :id="'help-text-' + this.id"></div>
</div>
<div v-else>
  <div v-html="model"></div>
</div>
</template>

<script>
import Questions from './Questions.vue'

export default {
  name: 'Section',
  props: {
    model: Object
  },
  components: {
    
  },
  data: function () {
    return {
      id: null
    }
  },
  mounted: function () {
    this.id = this.generateId();

    if(this.model.fileName && this.model.preLoad) {
      this.loadHelpText('#help-text-' + this.id, this.model.fileName);
    }
  },
  methods: {
    generateId: function guid() {
      return Math.floor((1 + Math.random()) * 0x10000)
            .toString(16)
            .substring(1);
    },

    loadHelpText: function (target, fileName) {
      $.get(fileName, function(data) {
        $(target).html(data);
      })
    }
  }
}
</script>

<style scoped lang="scss">
</style>
