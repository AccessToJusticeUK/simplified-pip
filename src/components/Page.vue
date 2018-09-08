<template>
  <article>
    <section>
        <header>
            <h1 v-if="model.title">{{model.title}}</h1>
            <small v-if="model.description">{{ model.description }}</small>
        </header>
        <div class="form">
            <Questions :items="model.questions" />
        </div>
        <footer>
            {{ pageNumber }}
        </footer>
    </section>
    <aside v-if="model.guidance" v-html="model.guidance" />
  </article>
</template>

<script>
import Questions from './Questions.vue'

export default {
  name: 'Section',
  props: {
    model: Object,
    pageNumber: Number
  },
  components: {
    Questions
  }
}
</script>

<style scoped lang="scss">
$grey-colour: rgb(102, 102, 102);
$border-colour: rgb(210, 210, 210);

$section-padding: 50px;
$section-margin-bottom: 37px;

article {
  display: flex;
  flex-direction: row;
  min-height: 1100px;
}

section {
  display: flex;
  flex-direction: column;
  padding: $section-padding;

  background-color: white;
  margin-bottom: $section-margin-bottom;
  width: 780px;
  box-sizing: border-box;
  -webkit-box-shadow: 5px 5px 10px rgba(204, 204, 204, 0.349019607843137);
  -moz-box-shadow: 5px 5px 10px rgba(204, 204, 204, 0.349019607843137);
  box-shadow: 5px 5px 10px rgba(204, 204, 204, 0.349019607843137);

  page-break-inside: avoid;
  page-break-after: always;

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

aside {
  width: 300px;
  margin-top: 50px;
  margin-left: 25px;
  margin-bottom: calc($section-margin-bottom + $section-padding);

  font-size: 14px;
  font-weight: 300;
  color: #333;
}
</style>
