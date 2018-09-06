<template>
  <div id="app">
    <SideNav />
    <div id="content">

      <Page pageNumber="1" :model="page_1" />

    </div>
  </div>
</template>

<script>
import SideNav from "./components/SideNav.vue";
import Page from "./components/Page.vue";

export default {
  name: "app",
  components: {
    SideNav,
    Page
  },
  data: function() {
    return {
      page_1: {
        title: "Section 1",
        description: "Smething",
        guidance: "another something",

        questions: [
          {
            id: "1",
            title: "First question",
            type: "single-line-textbox",
            placeholder: "Enter something",
            description: ""
          },
          {
            id: "9",
            title: "",
            type: "subsection",
            "heading": "About your health professional",
            "sub_heading": "If we need additional information we may contact the health professionals that support you."
            
          },
          {
            id: "3",
            title: "Multi Line question",
            type: "multi-line-textbox",
            placeholder: "Enter something 2"
          },
          {
            id: "4",
            title: "Radio Group question",
            type: "radio-group",
            guidance: "string",
            options: {
              key: "question-4",
              items: [
                {
                  title: "yes"
                },
                {
                  title: "no"
                },
                {
                  title: "sometimes"
                }
              ]
            }
          }
        ]
      }
    };
  }
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Open+Sans:300,400,400i,700");

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
  font-family: "Open Sans Light", "Open Sans Regular", "Open Sans", sans-serif;
  font-weight: 300;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  display: flex;
  justify-content: flex-start;

.guidance-page {
  font-size: 14px;
  font-weight: 300;
  color: #333;

}
.question h1.title {
  font-size: 16px;
  color: #333;
  font-weight: 400;
  line-height: 22px;
}

.question.single-line input[type=text] {
  width: 100%;
  padding: 5px;
  font-size: 14px;
  color: #333;
  font-weight: 400;
  border-style: solid;
  border-left-width: 3px;
  border-left-color: #ff6600;
  border-top-width: 1px;
  border-top-color: #e4e4e4;
  border-right-width: 1px;
  border-right-color: #e4e4e4;
  border-bottom-width: 1px;
  border-bottom-color: #e4e4e4;
}

.question.multi-line textarea {
  width: 100%;
  padding: 5px;
  font-size: 14px;
  color: #333;
  font-weight: 400;
  border-style: solid;
  border-left-width: 3px;
  border-left-color: #ff6600;
  border-top-width: 1px;
  border-top-color: #e4e4e4;
  border-right-width: 1px;
  border-right-color: #e4e4e4;
  border-bottom-width: 1px;
  border-bottom-color: #e4e4e4;
}

::placeholder {
color: #999;
font-style: italic;
}

  #content {
    margin-top: 95px;
    display: flex;
    flex-direction: column;
  }
}
</style>
