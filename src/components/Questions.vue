<template>

    <div class="questions">
        <div class="question" v-for="question in items" >

            <h1 class="title">{{question.title}}</h1>

            <div class="description">
                <HelpText :model="question.description" />
            </div>

            <SingleLineTextBox
                v-if="question.type=='single-line-textbox'"
                :placeholder="question.placeholder" />

            <MultiLineTextBox
                v-if="question.type=='multi-line-textbox'"
                :placeholder="question.placeholder" />

            <RadioGroup
                v-if="question.type=='radio-group'"
                :options="question.options" />

            <Table
                v-if="question.type=='table'"
                :columns="question.columns" />

            <div v-if="question.type=='subsection'">
                <div class="subsection">
                    <h2 v-if="question.heading">{{question.heading}}</h2>
                    <div v-if="question.sub_heading">{{question.sub_heading}}</div>
                </div>
            </div>

        </div>
    </div>
</template>

<style scoped lang="scss">
</style>

<script>
import SingleLineTextBox from './questionTypes/SingleLineTextBox.vue'
import MultiLineTextBox from './questionTypes/MultiLineTextBox.vue'
import RadioGroup from './questionTypes/RadioGroup.vue'
import Table from './questionTypes/Tables.vue'
import HelpText from './HelpText.vue'

export default {
  name: 'Questions',
  props: {
    items: Array
  },
  components: {
    SingleLineTextBox,
    MultiLineTextBox,
    RadioGroup,
    Table,
    HelpText
  },
  data: function () {
    return {}
  }
}
</script>
