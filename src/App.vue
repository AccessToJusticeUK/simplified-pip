<template>
  <div id="app">
    <SideNav />
    <div id="content">

      <Page pageNumber="1" :model="page_1" />
      <Page pageNumber="2" :model="page_2" />
      <Page pageNumber="3" :model="page_3" />

    </div>
  </div>
</template>

<script>
import SideNav from './components/SideNav.vue'
import Page from './components/Page.vue'

export default {
  name: 'app',
  components: {
    SideNav,
    Page
  },
  data: function () {
    return {
      page_1: {
        title: 'Section 1',
        description: '',
        guidance: "<div id=\"u75_text\" class=\"text \"><p style=\"font-size:20px;line-height:18px;\"><span style=\"font-family:'Open Sans Light', 'Open Sans Regular', 'Open Sans';font-weight:300;font-style:normal;\">Welcome to Simplified PiP</span><span style=\"font-family:'Open Sans';font-weight:400;font-style:normal;font-size:16px;\"> </span></p><p style=\"font-size:14px;line-height:18px;\"><span style=\"font-family:'Open Sans';font-weight:400;font-style:normal;\">for agencies assisting clients</span><span style=\"font-family:'Open Sans';font-weight:400;font-style:normal;font-size:13px;\"> </span></p><p style=\"font-size:13px;line-height:6px;\"><span style=\"font-family:'Open Sans';font-weight:400;font-style:normal;\"><br></span></p><p style=\"font-size:13px;line-height:18px;\"><span style=\"font-family:'Open Sans';font-weight:400;font-style:normal;\"><br></span></p><p style=\"font-size:13px;line-height:18px;\"><span style=\"font-family:'Open Sans';font-weight:400;font-style:normal;\">This form will allow you to type up a PiP application and then print it in a format for submission to DWP. </span></p><p style=\"font-size:13px;line-height:18px;\"><span style=\"font-family:'Open Sans';font-weight:400;font-style:normal;\"><br></span></p><p style=\"font-size:13px;line-height:18px;\"><span style=\"font-family:'Open Sans Italic', 'Open Sans Regular', 'Open Sans';font-weight:400;font-style:italic;\">Please note that in this current version you will need to add these print outs to the DWP supplied form and post them together.</span></p><p style=\"font-size:13px;line-height:18px;\"><span style=\"font-family:'Open Sans';font-weight:400;font-style:normal;\"><br></span></p><p style=\"font-size:13px;line-height:18px;\"><span style=\"font-family:'Open Sans';font-weight:400;font-style:normal;\"><br></span></p><p style=\"font-size:11px;line-height:18px;\"><span style=\"font-family:'Open Sans Light', 'Open Sans Regular', 'Open Sans';font-weight:300;font-style:normal;\">The aim of this form is to help with assisting a client through the PiP application process. The form allows you to edit and change details of the application as you progress through the interview, resulting in a printed form that is fast to produce and easy to read.</span></p><p style=\"font-size:11px;line-height:18px;\"><span style=\"font-family:'Open Sans Light', 'Open Sans Regular', 'Open Sans';font-weight:300;font-style:normal;\"><br></span></p><p style=\"font-size:11px;line-height:18px;\"><span style=\"font-family:'Open Sans Light', 'Open Sans Regular', 'Open Sans';font-weight:300;font-style:normal;\">We also offer advice and tips to the right of the form to assist you with the completion of the form alongside the descriptors to make sure you accurately give the DWP the information they need to asses the application.</span></p><p style=\"font-size:11px;line-height:18px;\"><span style=\"font-family:'Open Sans Light', 'Open Sans Regular', 'Open Sans';font-weight:300;font-style:normal;\"><br></span></p><p style=\"font-size:11px;line-height:18px;\"><span style=\"font-family:'Open Sans Light', 'Open Sans Regular', 'Open Sans';font-weight:300;font-style:normal;\">This is an evolving project and we welcome your feedback. Please let us know what you think.</span></p>        </div>",

        questions: [
          {
            id: '1',
            title: 'Name',
            type: 'single-line-textbox',
            placeholder: 'Applicants full legal name',
            description: ''
          },
          {
            id: '3',
            title: 'Address',
            type: 'multi-line-textbox',
            placeholder: 'Applicants address'
          },
          {
            id: '4',
            title: 'N.I. Number',
            type: 'single-line-textbox',
            placeholder: 'Applicants NI Number e.g AA 11 22 33 B',
            description: ''
          },
          {
            id: '5',
            title: '',
            type: 'subsection',
            'heading': 'About your health professional',
            'sub_heading': 'If we need additional information we may contact the health professionals that support you.'

          },
          // {
          //   id: '6',
          //   title: 'Q1 Tell us about the professional(s) best placed to advise us on how your health condition or disability affects you',
          //   type: 'table',
          //   placeholder: '',
          //   description: 'For example, a GP, hospital doctor, specialist nurse, community psychiatric nurse, occupational therapist, physiotherapist, social worker, counsellor, or support worker.'
          // },
          {
            id: '7',
            title: 'Multi Line question',
            type: 'multi-line-textbox',
            placeholder: 'Enter something 2'
          },
          {
            id: '8',
            title: 'Radio Group question',
            type: 'radio-group',
            guidance: 'string',
            options: {
              key: 'question-4',
              items: [
                {
                  title: 'yes'
                },
                {
                  title: 'no'
                },
                {
                  title: 'sometimes'
                }
              ]
            }
          }
        ]
      },
      page_2: {
        title: 'Section 2 – About your health condition or disability',
        description: 'Use page 7 of the Information Booklet to help you answer these questions.',
        guidance: '',
        questions: [
          {
            id: '8',
            title: 'Radio Group question',
            type: 'radio-group',
            guidance: 'string',
            options: {
              key: 'question-4',
              items: [
                {
                  title: 'yes'
                },
                {
                  title: 'no'
                },
                {
                  title: 'sometimes'
                }
              ]
            }
          },
          {
            id: '9',
            title: 'Q1 Tell us about the professional(s) best placed to advise us on how your health condition or disability affects you',
            type: 'table',
            placeholder: '',
            description: 'For example, a GP, hospital doctor, specialist nurse, community psychiatric nurse, occupational therapist, physiotherapist, social worker, counsellor, or support worker.'
          }

        ]
      },
      page_3: {
        title: 'Section 2 – About your health condition or disability',
        description: '',
        guidance: '',
        questions: [
          {
            id: '10',
            title: 'Q2b Tell us about:',
            type: 'multi-line-textbox',
            placeholder: '',
            description: '<li>Tablets or other medication you’re taking or will be taking and the dosage</li><li>Any treatments you’re having or will be having, such as chemotherapy, physiotherapy or dialysis</li><li>Any side effects these have on you</li>'
          }

        ]

      }
    }
  }
}
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
