<template>
  <article>
    <section>
        <header>
            <h2 v-if="title">{{ title }}</h2>
            <small v-if="description">{{ description }}</small>
        </header>
        <div class="form">
          <slot>This page has no content</slot>
            <!-- <Questions :items="model.questions" /> -->
        </div>
        <footer>
            {{ pageNumber }}
        </footer>
    </section>
    <aside>
      <slot name="guidance" />
    </aside>
  </article>
</template>

<script>
import Questions from './Questions.vue'

export default {
  name: 'Page',
  props: {
    title: String,
    description: String,
    pageNumber: Number
  },
  components: {
    Questions
  }
}
</script>

<style scoped lang="scss">
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

  footer {
    align-self: flex-end;
    text-align: right;
    margin-top: auto; // push the footer to the bottom
  }
}

aside {
  width: 258px;
  margin-left: 25px;
  margin-bottom: calc($section-margin-bottom + $section-padding);

  font-size: 13px;
  font-weight: 400;
  color: #333;

  header {
    h1, h2 {
      margin: 0;
    }
    h1 {
      font-size: 1.4em;
    }
    h2 {
      font-size: 1em;
    }
  }

  small {
    font-size: 0.9em;
  }
}
</style>
