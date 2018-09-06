<template>
    <div class="section">
        <section>
            <header>
                <h1 v-if="model.title">{{model.title}}</h1>
                <small v-if="model.description">{{ model.description }}</small>
                <div v-if="model.guidance" v-html="model.guidance"></div>
            </header>
            <div class="form">
                <Questions :items="model.questions" />   
            </div>
            <footer>
                {{ pageNumber }}
            </footer>
        </section>
    </div>
</template>

<script>
import Questions from "./Questions.vue"

export default {
  name: "Section",
  props: {
    model: Object,
    pageNumber: String
  },
  components: {
    Questions
  }
};
</script>

<style scoped lang="scss">
$grey-colour: rgb(102, 102, 102);
$border-colour: rgb(210, 210, 210);

section {
  display: flex;
  flex-direction: column;
  padding: 50px;

  background-color: white;
  margin-bottom: 37px;
  height: 1100px;
  width: 780px;
  -webkit-box-shadow: 5px 5px 10px rgba(204, 204, 204, 0.349019607843137);
  -moz-box-shadow: 5px 5px 10px rgba(204, 204, 204, 0.349019607843137);
  box-shadow: 5px 5px 10px rgba(204, 204, 204, 0.349019607843137);

  & > header {
    color: $grey-colour;

    & > h1 {
      border-bottom: 1px solid $border-colour;
    }
  }

  footer {
    align-self: flex-end;
    text-align: right;
    margin-top: auto; // push the footer to the bottom
  }
}
</style>
