<template>
    <div class="section">
        <section>
            <header>
                <h1>{{ header }}</h1>
                <small>{{ description }}</small>
            </header>
            <div class="form">
                <p>Form goes here</p>

                <div class="questions" v-for="question in questions">
                    <h1>{{question.title}}</h1>

                    <div v-if="question.type=='single-line-textbox'">
                        <input type="text" placeholder="Enter whatever" />
                    </div>
                </div>
            </div>
            <footer>
                {{ pageNumber }}
            </footer>
        </section>
    </div>
</template>

<script>
export default {
  name: 'Section',
  props: {
    header: String,
    description: String,
    pageNumber: String
    
  },
  data: function () {
      return {
          questions: [
            {
                "id": "1",
                "title": "First question",
                "type": "single-line-textbox",
            },
            {
                "id": "1",
                "title": "Second question",
                "type": "single-line-textbox",
            },
            {
                "id": "1",
                "title": "Second question",
                "type": "multi-line-textbox",
            }
        ]
      }
  }
}
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
