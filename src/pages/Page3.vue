<template>
    <Page page-number="3" title="Section 2 – About your health condition or disability">

        <Question number="2b" text="Tell us about:" />
        <ul>
          <li>Tablets or other medication you’re taking or will be taking and the dosage</li>
          <li>Any treatments you’re having or will be having, such as chemotherapy, physiotherapy or dialysis</li>
          <li>Any side effects these have on you</li>
        </ul>

        <MultiLineTextBox id="healthDetails" rows="15"
                          placeholder="e.g. Oramorph 2mg 5 times per day, results in insomnia and restlessness.">
            <div>
              Be sure to include any contraindications, i.e. medication that you cannot take while taking another type of medication.
            </div>
        </MultiLineTextBox>
        <MultiLineTextBox id="healthDetails" rows="15" label="Test"
                          placeholder="e.g. Oramorph 2mg 5 times per day, results in insomnia and restlessness.">
            <div>
              Be sure to include any contraindications, i.e. medication that you cannot take while taking another type of medication.
            </div>
        </MultiLineTextBox>
    </Page>
</template>

<script>
import Page from '../components/Page.vue'
import Question from '../components/Question.vue'
import SingleLineTextBox from '../components/questionTypes/SingleLineTextBox.vue'
import MultiLineTextBox from '../components/questionTypes/MultiLineTextBox.vue'
import Table from '../components/questionTypes/Table.vue'
import Divider from '../components/Divider.vue'

export default {
  components: {
    Page,
    Question,
    SingleLineTextBox,
    MultiLineTextBox,
    Table,
    Divider
  }
}
</script>
