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

                    <SingleLineTextBox 
                        v-if="question.type=='single-line-textbox'"
                        :placeholder="question.placeholder" />
                    <MultiLineTextBox 
                        v-if="question.type=='multi-line-textbox'"
                        :placeholder="question.placeholder" />
                        
                </div>
            </div>
            <footer>
                {{ pageNumber }}
            </footer>
        </section>
    </div>
</template>

<script>
import SingleLineTextBox from './questionTypes/SingleLineTextBox.vue'
import MultiLineTextBox from './questionTypes/MultiLineTextBox.vue'

export default {
  name: 'Section',
  props: {
    header: String,
    description: String,
    pageNumber: String
    
  },
  components: {
      SingleLineTextBox,
      MultiLineTextBox
  },
  data: function () {
      return {
          questions: [
            {
                "id": "1",
                "title": "First question",
                "type": "single-line-textbox",
                "placeholder": "Enter something"
            },
            {
                "id": "1",
                "title": "Second question",
                "type": "single-line-textbox",
                "placeholder": "Enter something 2"
            },
            {
                "id": "1",
                "title": "Multi Line question",
                "type": "multi-line-textbox",
                "placeholder": "Enter something 2"

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
