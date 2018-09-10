<template>
    <Page page-number="2" title="Section 2 – About your health condition or disability"
          description="Use page 7 of the Information Booklet to help you answer these questions.">

        <Question number="2a" text="Tell us in the space below what your health conditions or disabilities are, and approximately when each of these started."
                  description="We will ask you how your health conditions or disabilities affect how you carry out day-to-day activities in the rest of the form." />

        <Tables :columns="[{
                  title: 'Name',
                  placeholder: 'Name',
                  widthPercent: null,
                  value: ''
                },
                {
                  title: 'Address',
                  placeholder: 'Address',
                  widthPercent: null,
                  value: ''
                },
                {
                  title: 'Profession',
                  placeholder: 'Profession',
                  widthPercent: null,
                  value: ''
                },
                {
                  title: 'Telephone',
                  placeholder: 'Telephone number',
                  widthPercent: null,
                  value: ''
                },
                {
                  title: 'When did you last see them? (approximate date)',
                  placeholder: 'Last date seen',
                  widthPercent: null,
                  value: ''
                }]">
            <SingleLineTextBox id="healthIssue" label="Health condition or disability" placeholder="e.g. Diabetes" />
            <SingleLineTextBox id="startDate" label="Approximate start date" placeholder="e.g. May 2017" />
        </Tables>
    </Page>
</template>

<script>
import Page from '../components/Page.vue'
import Question from '../components/Question.vue'
import SingleLineTextBox from '../components/questionTypes/SingleLineTextBox.vue'
import MultiLineTextBox from '../components/questionTypes/MultiLineTextBox.vue'
import Tables from '../components/questionTypes/Tables.vue'
import Divider from '../components/Divider.vue'

export default {
  components: {
    Page,
    Question,
    SingleLineTextBox,
    MultiLineTextBox,
    Tables,
    Divider
  }
}
</script>
