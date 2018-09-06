<template>
  <div id="app">
    <SideNav />
    <div id="content">
      <Section header="Section 1" 
        pageNumber="1" />
        <Section header="Section 1" 
        pageNumber="2" />
    </div>
  </div>
</template>

<script>
import SideNav from './components/SideNav.vue'
import Section from './components/Section.vue'

export default {
  name: 'app',
  components: {
    SideNav,
    Section
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Open+Sans:300,400,400i,700');

h1 {
  margin-top: 0;
  margin-bottom: 0;
  font-weight: normal;
}

body {
    background-color: rgba(242, 242, 242, 1);
    margin-top: 0;
}

#app {
  font-family: 'Open Sans Light', 'Open Sans Regular', 'Open Sans', sans-serif;
  font-weight: 300;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  display: flex;
  justify-content: flex-start;

  #content {
    margin-top: 95px;
    display: flex;
    flex-direction: column;
  }
}
</style>
