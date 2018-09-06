<template>
  <div id="app">
    <SideNav />
    <div id="content">

      <Page pageNumber="1" :model="page_1" />
      <Page pageNumber="2" :model="page_2" />
      <Page pageNumber="3" :model="page_3" />
      <Page pageNumber="4" :model="page_4" />

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
          // {
          //   id: "0",
          //   title: "Table",
          //   type: "table",
          //   columns: [
          //       {
          //         title: "yes",
          //         placeholder: "placeholder",
          //         widthPercent: null,
          //         value: ""
          //       },
          //       {
          //         title: "no",
          //         placeholder: "placeholder",
          //         widthPercent: null,
          //         value: ""
          //       },
          //       {
          //         title: "sometimes",
          //         placeholder: "placeholder",
          //         widthPercent: null,
          //         value: ""
          //       },
          //       {
          //         title: "sometimes",
          //         placeholder: "placeholder",
          //         widthPercent: null,
          //         value: ""
          //       }
          //     ]
          // },{
          //   id: "0",
          //   title: "Table 2",
          //   type: "table",
          //   columns: [
          //       {
          //         title: "yes",
          //         placeholder: "placeholder",
          //         value: "",
          //         widthPercent: null
          //       },
          //       {
          //         title: "no",
          //         placeholder: "placeholder",
          //         widthPercent: null,
          //         value: ""
          //       }
          //     ]
          // },
          {
            id: '1',
            title: 'First question',
            type: 'single-line-textbox',
            placeholder: 'Enter something',
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
          {
            id: '0',
            title: 'Q1 Tell us about the professional(s) best placed to advise us on how your health condition or disability affects you',
            type: 'table',
            description: 'For example, a GP, hospital doctor, specialist nurse, community psychiatric nurse, occupational therapist, physiotherapist, social worker, counsellor, or support worker.',

            columns: [
              {
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
              }
            ]
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
        guidance: '<div id="u201_text" class="text "><p><span>Be sure to include any contraindications, i.e. medication that you cannot take while taking another type of medication.</span></p></div>',
        questions: [
          {
            id: '10',
            title: 'Q2b Tell us about:',
            type: 'multi-line-textbox',
            placeholder: 'e.g. Oramorph 2mg 5 times per day, results, in insomnia and restlessness',
            description: '<li>Tablets or other medication you’re taking or will be taking and the dosage</li><li>Any treatments you’re having or will be having, such as chemotherapy, physiotherapy or dialysis</li><li>Any side effects these have on you</li>'
          }

        ]

      },
      page_4: {
        title: 'Section 3 – How your health condition or disability affects your day-to-day life',
        description: 'Tell us in the rest of this form how your health conditions or disabilities affect your day-to-day activities.',
        guidance: "<div id=\"u218\" class=\"ax_default heading_3\"><div id=\"u218_div\" class=\"\"></div><div id=\"u218_text\" class=\"text \"><p><span>Descriptors for Q3</span></p></div></div><div id=\"u219\" class=\"ax_default\"> <!-- Unnamed (Table Cell) --> <div id=\"u220\" class=\"ax_default table_cell\"> <img id=\"u220_img\" class=\"img \" src=\"https://dxlfb468n8ekd.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u220.png?token=f03071042117d73cb14780df81d37a7c\"> <div id=\"u220_text\" class=\"text \"> <p><span>a. Can prepare and cook a simple meal unaided.</span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id=\"u221\" class=\"ax_default table_cell\"> <img id=\"u221_img\" class=\"img \" src=\"https://d2t44wh9rnwl5y.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u221.png?token=5a17e2f927a6275c9dcfeb5112be14c5\"> <div id=\"u221_text\" class=\"text \"> <p><span>0 points</span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id=\"u222\" class=\"ax_default table_cell\"> <img id=\"u222_img\" class=\"img \" src=\"https://d26uhratvi024l.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u222.png?token=1cc055114f55020c92f1c651482a7dd5\"> <div id=\"u222_text\" class=\"text \"> <p><span style=\"font-family:'Open Sans';font-weight:400;\">b. Needs to use an aid or appliance to be able to either prepare or cook a simple meal.</span><span style=\"font-family:'Open Sans Bold', 'Open Sans Regular', 'Open Sans';font-weight:700;\"> </span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id=\"u223\" class=\"ax_default table_cell\"> <img id=\"u223_img\" class=\"img \" src=\"https://d2v8ggac1o0f6z.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u223.png?token=60386fb5a2a7c314518008740ebbe22e\"> <div id=\"u223_text\" class=\"text \"> <p><span>2 points</span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id=\"u224\" class=\"ax_default table_cell\"> <img id=\"u224_img\" class=\"img \" src=\"https://dxlfb468n8ekd.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u224.png?token=676bcfe19995d66181203a710f6facba\"> <div id=\"u224_text\" class=\"text \"> <p><span style=\"font-family:'Open Sans';font-weight:400;\">c. Cannot cook a simple meal using a conventional cooker but is able to do so using a microwave.</span><span style=\"font-family:'Open Sans Bold', 'Open Sans Regular', 'Open Sans';font-weight:700;\"> </span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id=\"u225\" class=\"ax_default table_cell\"> <img id=\"u225_img\" class=\"img \" src=\"https://d2t44wh9rnwl5y.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u225.png?token=0b54635d312b84dd128efe22b617d2e7\"> <div id=\"u225_text\" class=\"text \"> <p><span>2 points</span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id=\"u226\" class=\"ax_default table_cell\"> <img id=\"u226_img\" class=\"img \" src=\"https://d26uhratvi024l.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u226.png?token=8ff4d47ebd1a4729ab93fdfcc0d7f89e\"> <div id=\"u226_text\" class=\"text \"> <p><span>d. Needs prompting to be able to either prepare or&nbsp; cook a simple meal.</span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id=\"u227\" class=\"ax_default table_cell\"> <img id=\"u227_img\" class=\"img \" src=\"https://d2v8ggac1o0f6z.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u227.png?token=c7e37c44cddd7bb89ff556793cefef3a\"> <div id=\"u227_text\" class=\"text \"> <p><span>2 points</span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id=\"u228\" class=\"ax_default table_cell\"> <img id=\"u228_img\" class=\"img \" src=\"https://dxlfb468n8ekd.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u228.png?token=dc8ab7ec75b9bf5d7125bfcb665ebeda\"> <div id=\"u228_text\" class=\"text \"> <p><span style=\"font-family:'Open Sans';font-weight:400;\">e. Needs supervision or assistance to either prepare or cook a simple meal.</span><span style=\"font-family:'Open Sans Bold', 'Open Sans Regular', 'Open Sans';font-weight:700;\"> </span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id=\"u229\" class=\"ax_default table_cell\"> <img id=\"u229_img\" class=\"img \" src=\"https://d2t44wh9rnwl5y.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u229.png?token=0b65653af1a7a9401fdbcb2ad6ea17ed\"> <div id=\"u229_text\" class=\"text \"> <p><span>4 points</span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id=\"u230\" class=\"ax_default table_cell\"> <img id=\"u230_img\" class=\"img \" src=\"https://dxlfb468n8ekd.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u230.png?token=dcc40ba5cfd554f6e56af6dd1fb2f748\"> <div id=\"u230_text\" class=\"text \"> <p><span style=\"font-family:'Open Sans';font-weight:400;\">f. Cannot prepare and cook food.</span><span style=\"font-family:'Open Sans Bold', 'Open Sans Regular', 'Open Sans';font-weight:700;\"> </span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id=\"u231\" class=\"ax_default table_cell\"> <img id=\"u231_img\" class=\"img \" src=\"https://d2t44wh9rnwl5y.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u231.png?token=b4ee4fdf316bfe940e3489adf585d809\"> <div id=\"u231_text\" class=\"text \"> <p><span>8 points</span></p> </div> </div> </div><div id=\"u233\" class=\"ax_default box_1\"> <div id=\"u233_div\" class=\"\"></div> <div id=\"u233_text\" class=\"text \"> <p><span>It's helpful to base your answers on this example: peel, chop and boil 2 large potatoes, open a tin of sweetcorn and fry a small piece of meat or fish.</span></p><p><span><br></span></p><p><span>Applicants with a hearing impairment or visual impairment may also have problems preparing food.</span></p> </div> </div><div id=\"u234\" class=\"ax_default box_1\"> <div id=\"u234_div\" class=\"\"></div> <div id=\"u234_text\" class=\"text \"> <p><span>Never miss out an aid off the list if you think it's obvious.</span></p><p><span><br></span></p><p><span>Remember a prosthetic limb and a walking stick are both considered aids.</span></p> </div> </div>"

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

.subsection h2 {
  font-size: 20px;
  color: #666666;
  font-weight: 200;
}

.subsection div {
  font-size: 12px;
  color: #797979;
  line-height: 18px;
}

.question h1.title {
  font-size: 16px;
  color: #333;
  font-weight: 600;
}

.question .description {
  font-size: 12px;
  font-weight: 400;
  color: #666666;
}

.question .radio-group .option {
  font-size: 18px;
  font-weight: 400;
  padding-right: 10px;
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

  #content {
    margin-top: 95px;
    display: flex;
    flex-direction: column;
  }

  .question table {
    width: 100%;

    textarea {
      width: 100%;
    }
  }
}
</style>
