<template>
    <Page page-number="1" title="Section 1">
        <SingleLineTextBox id="name" label="Name"
                           placeholder="Applicant's full legal name" />

        <MultiLineTextBox id="address" label="Address"
                          placeholder="Applicant's address" rows="5" />

        <SingleLineTextBox id="ni-number" label="N.I. Number"
                           placeholder="Applicant's NI Number e.g. AA 11 22 33 B" half="true" />

        <Divider title="About your health professionals"
                 description="If we need additional information we may contact the health professionals that support you." />

        <Question number="1" text="Tell us about the professional(s) best placed to advise us on how your health condition or disability affects you"
                  description="For example, a GP, hospital doctor, specialist nurse, community psychiatric nurse, occupational therapist, physiotherapist, social worker, counsellor, or support worker." />

        <template slot="guidance">
            <div>
                <header>
                    <h1>Welcome to Simplified PiP</h1>
                    <h2>for agencies assisting clients</h2>
                </header>
                <p>
                    This form will allow you to type up a PiP application and then print it in a format for submission to DWP.
                </p>
                <p>
                    <em>Please note that in this current version you will need to add these print outs to the DWP supplied form and post them together.</em>
                </p>
                <p>&nbsp;</p>
                <p>
                    <small>
                        The aim of this form is to help with assisting a client through the PiP application process.
                        The form allows you to edit and change details of the application as you progress through the interview,
                        resulting in a printed form that is fast to produce and easy to read.
                    </small>
                </p>
                <p>
                    <small>
                        We also offer advice and tips to the right of the form to assist you with the completion of the form
                        alongside the descriptors to make sure you accurately give the DWP the information they need to asses the application.
                    </small>
                </p>
                <p>
                    <small>This is an evolving project and we welcome your feedback. Please let us know what you think.</small>
                </p>
            </div>
        </template>
    </Page>
</template>

<script>
import Page from '../components/Page.vue'
import Question from '../components/Question.vue'
import SingleLineTextBox from '../components/questionTypes/SingleLineTextBox.vue'
import MultiLineTextBox from '../components/questionTypes/MultiLineTextBox.vue'
import Divider from '../components/Divider.vue'

export default {
  components: {
    Page,
    Question,
    SingleLineTextBox,
    MultiLineTextBox,
    Divider
  }
}
</script>
