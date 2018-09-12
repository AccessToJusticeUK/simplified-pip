<template>
  <div id="app">
    <SideNav />
    <div id="content">

      <div v-for="page in pages" v-bind:key="page.pageNum">
        <Page :pageNumber="page.pageNum" :model="page" />
      </div>

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
  data: function() {
    return {
      pages: [
        /* Page 1 */
        {
          pageNum: 1,
          title: "Section 1",
          description: "",
          guidance: {
            fileName: "g.html",
            preLoad: true,
            cssClass: "guidance-page"
          },

          questions: [
            {
              id: "1",
              title: "Name",
              type: "single-line-textbox",
              placeholder: "Enter your name here",
              description: ""
            },
            {
              id: "3",
              title: "Address",
              type: "multi-line-textbox",
              placeholder: "Applicants address"
            },
            {
              id: "4",
              title: "N.I. Number",
              type: "single-line-textbox",
              placeholder: "Applicants NI Number e.g AA 11 22 33 B",
              description: ""
            },
            {
              id: "5",
              title: "",
              type: "subsection",
              heading: "About your health professional",
              sub_heading:
                "If we need additional information we may contact the health professionals that support you."
            },
            {
              id: "0",
              title:
                "Q1 Tell us about the professional(s) best placed to advise us on how your health condition or disability affects you",
              type: "table",
              description:
                "For example, a GP, hospital doctor, specialist nurse, community psychiatric nurse, occupational therapist, physiotherapist, social worker, counsellor, or support worker.",

              columns: [
                {
                  title: "Name",
                  placeholder: "Name",
                  widthPercent: null,
                  value: ""
                },
                {
                  title: "Address",
                  placeholder: "Address",
                  widthPercent: null,
                  value: ""
                },
                {
                  title: "Profession",
                  placeholder: "Profession",
                  widthPercent: null,
                  value: ""
                },
                {
                  title: "Telephone",
                  placeholder: "Telephone number",
                  widthPercent: null,
                  value: ""
                },
                {
                  title: "When did you last see them? (approximate date)",
                  placeholder: "Last date seen",
                  widthPercent: null,
                  value: ""
                }
              ]
            },
            {
              id: "8",
              title: "Radio Group question",
              type: "radio-group",
              guidance: "string",
              options: {
                key: "question-4",
                items: [
                  {
                    title: "yes"
                  },
                  {
                    title: "no"
                  },
                  {
                    title: "sometimes"
                  }
                ]
              }
            }
          ]
        },
        /* Page 2 */
        {
          pageNum: 2,
          title: "Section 2 – About your health condition or disability",
          description:
            "Use page 7 of the Information Booklet to help you answer these questions.",
          guidance: "",
          questions: [
            {
              id: "8",
              title: "Radio Group question",
              type: "radio-group",
              guidance: "string",
              options: {
                key: "question-4",
                items: [
                  {
                    title: "yes"
                  },
                  {
                    title: "no"
                  },
                  {
                    title: "sometimes"
                  }
                ]
              }
            },
            {
              id: "9",
              title:
                "Q1 Tell us about the professional(s) best placed to advise us on how your health condition or disability affects you",
              type: "table",
              placeholder: "",
              description:
                "For example, a GP, hospital doctor, specialist nurse, community psychiatric nurse, occupational therapist, physiotherapist, social worker, counsellor, or support worker."
            }
          ]
        },
        /* Page 3 */
        {
          pageNum: 3,
          title: "Section 2 – About your health condition or disability",
          description: "",
          guidance:
            '<div id="u201_text" class="text "><p><span>Be sure to include any contraindications, i.e. medication that you cannot take while taking another type of medication.</span></p></div>',
          questions: [
            {
              id: "10",
              title: "Q2b Tell us about:",
              type: "multi-line-textbox",
              placeholder:
                "e.g. Oramorph 2mg 5 times per day, results, in insomnia and restlessness",
              description:
                "<li>Tablets or other medication you’re taking or will be taking and the dosage</li><li>Any treatments you’re having or will be having, such as chemotherapy, physiotherapy or dialysis</li><li>Any side effects these have on you</li>"
            }
          ]
        },

        /* Page 4 */
        {
          pageNum: 4,
          title:
            "Section 3 – How your health condition or disability affects your day-to-day life",
          description:
            "Tell us in the rest of this form how your health conditions or disabilities affect your day-to-day activities.",
          guidance:
            '<div id="u218" class="ax_default heading_3"><div id="u218_div" class=""></div><div id="u218_text" class="text "><p><span>Descriptors for Q3</span></p></div></div><div id="u219" class="ax_default"> <!-- Unnamed (Table Cell) --> <div id="u220" class="ax_default table_cell"> <img id="u220_img" class="img " src="https://dxlfb468n8ekd.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u220.png?token=f03071042117d73cb14780df81d37a7c"> <div id="u220_text" class="text "> <p><span>a. Can prepare and cook a simple meal unaided.</span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id="u221" class="ax_default table_cell"> <img id="u221_img" class="img " src="https://d2t44wh9rnwl5y.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u221.png?token=5a17e2f927a6275c9dcfeb5112be14c5"> <div id="u221_text" class="text "> <p><span>0 points</span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id="u222" class="ax_default table_cell"> <img id="u222_img" class="img " src="https://d26uhratvi024l.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u222.png?token=1cc055114f55020c92f1c651482a7dd5"> <div id="u222_text" class="text "> <p><span style="font-family:\'Open Sans\';font-weight:400;">b. Needs to use an aid or appliance to be able to either prepare or cook a simple meal.</span><span style="font-family:\'Open Sans Bold\', \'Open Sans Regular\', \'Open Sans\';font-weight:700;"> </span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id="u223" class="ax_default table_cell"> <img id="u223_img" class="img " src="https://d2v8ggac1o0f6z.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u223.png?token=60386fb5a2a7c314518008740ebbe22e"> <div id="u223_text" class="text "> <p><span>2 points</span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id="u224" class="ax_default table_cell"> <img id="u224_img" class="img " src="https://dxlfb468n8ekd.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u224.png?token=676bcfe19995d66181203a710f6facba"> <div id="u224_text" class="text "> <p><span style="font-family:\'Open Sans\';font-weight:400;">c. Cannot cook a simple meal using a conventional cooker but is able to do so using a microwave.</span><span style="font-family:\'Open Sans Bold\', \'Open Sans Regular\', \'Open Sans\';font-weight:700;"> </span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id="u225" class="ax_default table_cell"> <img id="u225_img" class="img " src="https://d2t44wh9rnwl5y.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u225.png?token=0b54635d312b84dd128efe22b617d2e7"> <div id="u225_text" class="text "> <p><span>2 points</span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id="u226" class="ax_default table_cell"> <img id="u226_img" class="img " src="https://d26uhratvi024l.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u226.png?token=8ff4d47ebd1a4729ab93fdfcc0d7f89e"> <div id="u226_text" class="text "> <p><span>d. Needs prompting to be able to either prepare or&nbsp; cook a simple meal.</span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id="u227" class="ax_default table_cell"> <img id="u227_img" class="img " src="https://d2v8ggac1o0f6z.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u227.png?token=c7e37c44cddd7bb89ff556793cefef3a"> <div id="u227_text" class="text "> <p><span>2 points</span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id="u228" class="ax_default table_cell"> <img id="u228_img" class="img " src="https://dxlfb468n8ekd.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u228.png?token=dc8ab7ec75b9bf5d7125bfcb665ebeda"> <div id="u228_text" class="text "> <p><span style="font-family:\'Open Sans\';font-weight:400;">e. Needs supervision or assistance to either prepare or cook a simple meal.</span><span style="font-family:\'Open Sans Bold\', \'Open Sans Regular\', \'Open Sans\';font-weight:700;"> </span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id="u229" class="ax_default table_cell"> <img id="u229_img" class="img " src="https://d2t44wh9rnwl5y.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u229.png?token=0b65653af1a7a9401fdbcb2ad6ea17ed"> <div id="u229_text" class="text "> <p><span>4 points</span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id="u230" class="ax_default table_cell"> <img id="u230_img" class="img " src="https://dxlfb468n8ekd.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u230.png?token=dcc40ba5cfd554f6e56af6dd1fb2f748"> <div id="u230_text" class="text "> <p><span style="font-family:\'Open Sans\';font-weight:400;">f. Cannot prepare and cook food.</span><span style="font-family:\'Open Sans Bold\', \'Open Sans Regular\', \'Open Sans\';font-weight:700;"> </span></p> </div> </div> <!-- Unnamed (Table Cell) --> <div id="u231" class="ax_default table_cell"> <img id="u231_img" class="img " src="https://d2t44wh9rnwl5y.cloudfront.net/gsc/1A51QE/89/6d/9f/896d9fc8865f40cdb1efd13a7834d720/images/simplified_pip_for_agencies/u231.png?token=b4ee4fdf316bfe940e3489adf585d809"> <div id="u231_text" class="text "> <p><span>8 points</span></p> </div> </div> </div><div id="u233" class="ax_default box_1"> <div id="u233_div" class=""></div> <div id="u233_text" class="text "> <p><span>It\'s helpful to base your answers on this example: peel, chop and boil 2 large potatoes, open a tin of sweetcorn and fry a small piece of meat or fish.</span></p><p><span><br></span></p><p><span>Applicants with a hearing impairment or visual impairment may also have problems preparing food.</span></p> </div> </div><div id="u234" class="ax_default box_1"> <div id="u234_div" class=""></div> <div id="u234_text" class="text "> <p><span>Never miss out an aid off the list if you think it\'s obvious.</span></p><p><span><br></span></p><p><span>Remember a prosthetic limb and a walking stick are both considered aids.</span></p> </div> </div>',
          questions: [
            {
              id: "8",
              title: "Q3 Preparing food ",
              type: "radio-group",
              guidance:
                '<div id="u234" class="ax_default box_1"> <div id="u234_div" class=""></div> <div id="u234_text" class="text "> <p><span>Never miss out an aid off the list if you think it\'s obvious.</span></p><p><span><br></span></p><p><span>Remember a prosthetic limb and a walking stick are both considered aids.</span></p> </div> </div>',
              options: {
                key: "question-4",
                items: []
              }
            },
            {
              id: "8",
              title:
                "Q3a Do you need to use an aid or appliance to prepare or cook a simple meal?",
              type: "radio-group",
              guidance:
                "Aids and appliances include things like: Perching stools, lightweight pots and pans, easy grip handles on utensils, single lever arm taps and liquid level indicators",
              options: {
                key: "question-3a",
                items: [
                  {
                    title: "yes"
                  },
                  {
                    title: "no"
                  },
                  {
                    title: "sometimes"
                  }
                ]
              }
            },
            {
              id: "8",
              title:
                "Q3b Do you need help from another person to prepare or cook a simple meal?",
              type: "radio-group",
              guidance:
                '<div id="u232" class="ax_default heading_2"> <div id="u232_div" class=""></div> <div id="u232_text" class="text "> <p><span style="font-family:\'Open Sans\';font-weight:400;">By this we mean: </span></p> <p><span style="font-family:\'Open Sans\';font-weight:400;">•&nbsp; &nbsp;&nbsp; Do they remind or motivate you to cook?</span></p> <p><span style="font-family:\'Open Sans\';font-weight:400;">•&nbsp; &nbsp;&nbsp; Do they plan the task for you?</span></p> <p><span style="font-family:\'Open Sans\';font-weight:400;">•&nbsp; &nbsp;&nbsp; Do they supervise you? </span></p> <p><span style="font-family:\'Open Sans\';font-weight:400;">•&nbsp; &nbsp;&nbsp; Do they physically help you?</span></p> <p><span style="font-family:\'Open Sans\';font-weight:400;">•&nbsp; &nbsp;&nbsp; Do they prepare all your food for you?</span></p> <p><span style="font-family:\'Open Sans\';font-weight:400;">This includes help you have </span><span style="font-family:\'Open Sans Bold\', \'Open Sans Regular\', \'Open Sans\';font-weight:700;">and</span><span style="font-family:\'Open Sans\';font-weight:400;"> help you need but don’t get.</span></p> </div></div>',
              options: {
                key: "question-3b",
                items: [
                  {
                    title: "yes"
                  },
                  {
                    title: "no"
                  },
                  {
                    title: "sometimes"
                  }
                ]
              }
            }
          ]
        },

        /* Page 5 */
        {
          pageNum: 5,
          title:
            "Section 3 – How your health condition or disability affects your day-to-day life ",
          description:
            "<div id=\"u253\" class=\"ax_default heading_2\"> <div id=\"u253_div\" class=\"\"></div> <div id=\"u253_text\" class=\"text \"> <p><span style=\"font-family:'Open Sans Bold', 'Open Sans Regular', 'Open Sans';font-weight:700;\">Extra information – Preparing food</span></p> <p><span style=\"font-family:'Open Sans';font-weight:400;\">Tell us more about any difficulties you have when </span><span style=\"font-family:'Open Sans Bold', 'Open Sans Regular', 'Open Sans';font-weight:700;\">preparing and cooking food</span><span style=\"font-family:'Open Sans';font-weight:400;\">:</span></p> <p><span style=\"font-family:'Open Sans';font-weight:400;\">•&nbsp; &nbsp;&nbsp; Tell us how your condition affects you doing this activity </span></p> <p><span style=\"font-family:'Open Sans';font-weight:400;\">•&nbsp; &nbsp;&nbsp; Tell us how you manage at the moment and the problems you have when you can’t do </span></p> <p><span style=\"font-family:'Open Sans';font-weight:400;\">&nbsp;&nbsp; &nbsp; &nbsp; this activity </span></p> <p><span style=\"font-family:'Open Sans';font-weight:400;\">•&nbsp; &nbsp;&nbsp; Tell us how long it takes you to prepare and cook food </span></p> <p><span style=\"font-family:'Open Sans';font-weight:400;\">•&nbsp; &nbsp;&nbsp; Does whether you can do this vary throughout the day? Tell us about good and bad</span></p> <p><span style=\"font-family:'Open Sans';font-weight:400;\">&nbsp;&nbsp; &nbsp; &nbsp; days </span></p> <p><span style=\"font-family:'Open Sans';font-weight:400;\">•&nbsp; &nbsp;&nbsp; Can you cook using an oven safely? If not, tell us why not</span></p> <p><span style=\"font-family:'Open Sans';font-weight:400;\">•&nbsp; &nbsp;&nbsp; Tell us about the aids or appliances you </span><span style=\"font-family:'Open Sans Bold', 'Open Sans Regular', 'Open Sans';font-weight:700;\">need</span><span style=\"font-family:'Open Sans';font-weight:400;\"> to use to help you prepare and cook </span></p> <p><span style=\"font-family:'Open Sans';font-weight:400;\">&nbsp;&nbsp; &nbsp; &nbsp; food </span></p> <p><span style=\"font-family:'Open Sans';font-weight:400;\">•&nbsp; &nbsp;&nbsp; Do you experience any other difficulties, </span><span style=\"font-family:'Open Sans Bold', 'Open Sans Regular', 'Open Sans';font-weight:700;\">either during or after the activity</span><span style=\"font-family:'Open Sans';font-weight:400;\">, like pain,</span></p> <p><span style=\"font-family:'Open Sans';font-weight:400;\">&nbsp;&nbsp; &nbsp; &nbsp; breathlessness or tiredness? </span></p> <p><span style=\"font-family:'Open Sans';font-weight:400;\">•&nbsp; &nbsp;&nbsp; Tell us about </span><span style=\"font-family:'Open Sans Bold', 'Open Sans Regular', 'Open Sans';font-weight:700;\">help you get from another person</span><span style=\"font-family:'Open Sans';font-weight:400;\"> when preparing food. This includes</span></p> <p><span style=\"font-family:'Open Sans';font-weight:400;\">&nbsp;&nbsp; &nbsp; &nbsp; help you have </span><span style=\"font-family:'Open Sans Bold', 'Open Sans Regular', 'Open Sans';font-weight:700;\">and</span><span style=\"font-family:'Open Sans';font-weight:400;\"> help you need but don’t get</span></p> </div></div>",
          guidance:
            '<div id="u258" class="ax_default box_1"> <div id="u258_div" class=""></div> <div id="u258_text" class="text "> <p><span>Try asking the applicant did they cook last night? Or When did they last cook a meal?</span></p><p><span><br></span></p><p><span>If they use aid/appliance, explain</span></p><p><span>- How they help and what would happen if they didn\'t use them?</span></p><p><span>- Did a health professional advise them to?</span></p><p><span>- Who supervises them, how often? Include any help they need but don\'t get.</span></p><p><span><br></span></p><p><span>If they heat food,</span></p><p><span>- Do they use a hob or microwave?</span></p><p><span>- Can they heat on a hob or would they use a microwave?</span></p> </div> </div>',
          questions: [
            {
              id: "3",
              title: "",
              type: "multi-line-textbox",
              placeholder: "type information here"
            }
          ]
        },

        /* Page 6 */
        {
          pageNum: 6,
          title:
            'Section 3 – How your health condition or disability affects your day-to-day life',
          description: '',
          guidance: '',
          questions: [

            {
              id: '8',
              title: 'Q4 Eating and drinking',
              type: 'radio-group',
              description:'',
              guidance:
                '',
              options: {
                key: 'question-4',
                items: []
              }
            },
            {
              id: '8',
              title:
                'Q4a Do you need to use an aid or appliance to eat and drink?',
              type: 'radio-group',
              description: '',
              guidance:
                '',
              options: {
                key: 'question-4a',
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
              id: '8',
              title:
                'Q4b Do you use a feeding tube or similar device to eat and drink?',
              type: 'radio-group',
              description: '',
              guidance:
                '',
              options: {
                key: 'question-4b',
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
              id: '8',
              title:
                'Q4c Do you need help from another person to eat and drink?',
              type: 'radio-group',
              description: '',
              guidance:
                '',
              options: {
                key: 'question-4c',
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



          ]
        },
        {
          pageNum: 7,
          title:
            'Section 3 – How your health condition or disability affects your day-to-day life ',
<<<<<<< HEAD
          description: "",
          guidance:'',
=======
          description: '',
          guidance: {
            fileName: 'pageGuidance/Guide-Page-07.html',
            preLoad: true,
            cssClass: 'guidance-page'
          },
>>>>>>> added all guidance's (up to p19)
          questions: [
            {
              id: '3',
              title: 'Extra information –Eating and drinking',
              type: 'multi-line-textbox',
              placeholder: 'type information here'
            }
          ]
        },
        {
          pageNum: 8,
          title:
            'Section 3 – How your health condition or disability affects your day-to-day life ',
          description: "",
          guidance:'',
          questions: [
            {
              id: '8',
              title:
                'Q5 Managing treatments',
              type: 'radio-group',
              description: '',
              guidance: '',
              options: {
                key: 'question-4',
                items: []
              }
            },
            {
              id: '8',
              title:
                'Q5a Do you need to use an aid or appliance to monitor your health conditions, take medication or manage home treatments?',
              type: 'radio-group',
              description: '',
              guidance:
                '',
              options: {
                key: 'question-5a',
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
              id: '8',
              title:
                'Q5b Do you need help from another person to monitor your health conditions, take medication or manage home treatments?',
              type: 'radio-group',
              description: '',
              guidance:
                '',
              options: {
                key: 'question-5b',
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
        {
          pageNum: 9,
          title:
            'Section 3 – How your health condition or disability affects your day-to-day life ',
<<<<<<< HEAD
          description: "",
          guidance:'',
=======
          description: '',
          guidance: {
            fileName: 'pageGuidance/Guide-Page-09.html',
            preLoad: true,
            cssClass: 'guidance-page'
          },
>>>>>>> added all guidance's (up to p19)
          questions: [
            {
              id: '3',
              title: 'Extra information – Managing treatments',
              description: '',
              type: 'multi-line-textbox',
              placeholder: 'type information here'
            }
          ]
        },
        {
          pageNum: 10,
          title:
            'Section 3 – How your health condition or disability affects your day-to-day life ',
          description: "",
          guidance:'',
          questions: [
            {
              id: '8',
              title:
                'Q6 Washing and bathing',
              type: 'radio-group',
              description: '',
              guidance: '',
              options: {
                key: 'question-6',
                items: []
              }
            },
            {
              id: '8',
              title:
                'Q6a Do you need to use an aid or appliance to wash and bathe yourself, including using a bath or shower?',
              type: 'radio-group',
              description: '',
              guidance:
                '',
              options: {
                key: 'question-6a',
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
              id: '8',
              title:
                'Q6b Do you need help from another person to wash and bathe?',
              type: 'radio-group',
              description: '',
              guidance:
                '',
              options: {
                key: 'question-6b',
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
        {
          pageNum: 11,
          title:
            'Section 3 – How your health condition or disability affects your day-to-day life ',
<<<<<<< HEAD
          description: "",
          guidance:'',
=======
          description: '',
          guidance: {
            fileName: 'pageGuidance/Guide-Page-11.html',
            preLoad: true,
            cssClass: 'guidance-page'
          },
>>>>>>> added all guidance's (up to p19)
          questions: [
            {
              id: '3',
              title: 'Extra information – Washing and bathing',
              description: "",
              type: 'multi-line-textbox',
              placeholder: 'type information here'
            }
          ]
        },
        {
          pageNum: 12,
          title:
            'Section 3 – How your health condition or disability affects your day-to-day life ',
          description: "",
          guidance:'',
          questions: [
            {
              id: '8',
              title:
                'Q7 Managing toilet needs',
              type: 'radio-group',
              description: '',
              guidance: '',
              options: {
                key: 'question-7',
                items: []
              }
            },
            {
              id: '8',
              title:
                'Q7a do you need to use an aid or appliance to use the toilet or manage incontinence?',
              type: 'radio-group',
              description: '',
              guidance:
                '',
              options: {
                key: 'question-7a',
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
              id: '8',
              title:
                'Q7b do you need help from another person to use the toilet or manage incontinence?',
              type: 'radio-group',
              description: '',
              guidance:
                '',
              options: {
                key: 'question-7b',
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
        {
          pageNum: 13,
          title:
            'Section 3 – How your health condition or disability affects your day-to-day life ',
<<<<<<< HEAD
          description: "",
          guidance:'',
=======
          description: '',
          guidance: {
            fileName: 'pageGuidance/Guide-Page-13.html',
            preLoad: true,
            cssClass: 'guidance-page'
          },
>>>>>>> added all guidance's (up to p19)
          questions: [
            {
              id: '3',
              title: 'Extra information – managing toilet needs',
              type: 'multi-line-textbox',
              description: '',
              placeholder: 'type information here'
            }
          ]
        },
        {
          pageNum: 14,
          title:
            'Section 3 – How your health condition or disability affects your day-to-day life ',
          description: "",
          guidance:'',
          questions: [
            {
              id: '8',
              title:
                'Q8 Dressing and undressing',
              type: 'radio-group',
              description: '',
              guidance: '',
              options: {
                key: 'question-8',
                items: []
              }
            },
            {
              id: '8',
              title:
                'Q8a do you need to use and aid or appliance to dress or undress?',
              type: 'radio-group',
              description: '',
              guidance:
                '',
              options: {
                key: 'question-8a',
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
              id: '8',
              title:
                'Q8b Do you need help from another person to dress or undress?',
              type: 'radio-group',
              description: '',
              guidance:
                '',
              options: {
                key: 'question-8b',
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
        {
          pageNum: 15,
          title:
            'Section 3 – How your health condition or disability affects your day-to-day life ',
<<<<<<< HEAD
          description: "",
          guidance:'',
=======
          description: '',
          guidance: {
            fileName: 'pageGuidance/Guide-Page-15.html',
            preLoad: true,
            cssClass: 'guidance-page'
          },
>>>>>>> added all guidance's (up to p19)
          questions: [
            {
              id: '3',
              title: 'Extra information – Dressing and undressing',
              description: '',
              type: 'multi-line-textbox',
              placeholder: 'type information here'
            }
          ]
        },
        {
          pageNum: 16,
          title:
            'Section 3 – How your health condition or disability affects your day-to-day life ',
          description: "",
          guidance:'',
          questions: [
            {
              id: '8',
              title:
                'Q9 Communicating',
              type: 'radio-group',
              description: '',
              guidance: '',
              options: {
                key: 'question-9',
                items: []
              }
            },
            {
              id: '8',
              title:
                'Q9a Do you need to use an aid or appliance to communicate with others?',
              type: 'radio-group',
              description: '',
              guidance:
                '',
              options: {
                key: 'question-9a',
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
              id: '8',
              title:
                'Q9b Do you need help from another person to communicate with others?',
              type: 'radio-group',
              description: '',
              guidance:
                '',
              options: {
                key: 'question-9b',
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
        {
          pageNum: 17,
          title:
            'Section 3 – How your health condition or disability affects your day-to-day life ',
<<<<<<< HEAD
          description: "",
          guidance:'',
=======
          description: '',
          guidance: {
            fileName: 'pageGuidance/Guide-Page-17.html',
            preLoad: true,
            cssClass: 'guidance-page'
          },
>>>>>>> added all guidance's (up to p19)
          questions: [
            {
              id: '3',
              title: 'Extra information – Communicating',
              description: '',
              type: 'multi-line-textbox',
              placeholder: 'type information here'
            }
          ]
        },
        {
          pageNum: 18,
          title:
            'Section 3 – How your health condition or disability affects your day-to-day life ',
          description: "",
          guidance:'',
          questions: [
            {
              id: '8',
              title:
                'Q10 Reading',
              type: 'radio-group',
              description: '',
              guidance: '',
              options: {
                key: 'question-10',
                items: []
              }
            },
            {
              id: '8',
              title:
                'Q10a Do you need to use an aid or appliance other than spectacles or contact lenses to read signs, symbols and words?',
              type: 'radio-group',
              description: '',
              guidance:
                '',
              options: {
                key: 'question-10a',
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
              id: '8',
              title:
                'Q10b Do you need help from another person to read or understand signs, symbols and words?',
              type: 'radio-group',
              description: '',
              guidance:
                '',
              options: {
                key: 'question-10b',
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
        {
          pageNum: 19,
          title:
            'Section 3 – How your health condition or disability affects your day-to-day life ',
<<<<<<< HEAD
          description: "",
          guidance:'',
=======
          description: '',
          guidance: {
            fileName: 'pageGuidance/Guide-Page-19.html',
            preLoad: true,
            cssClass: 'guidance-page'
          },
>>>>>>> added all guidance's (up to p19)
          questions: [
            {
              id: '3',
              title: 'Extra information – Reading',
              description: '',
              type: 'multi-line-textbox',
              placeholder: 'type information here'
            }
          ]
        },

      ]
    };
  }
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Open+Sans:300,400,400i,700");

h1 {
    margin-top: 0;
    margin-bottom: 0;
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
  
    .question {
      margin-bottom: 20px;
    }
    .question h1.title {
      font-size: 16px;
      color: #333;
      font-weight: 400;
      line-height: 22px;
    }
  
    .question.single-line input[type="text"] {
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
  
  textarea, input[type="text"] {
    font-size: 14px;
    font-family: inherit;
  }
    .question.multi-line textarea{
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
  
    ::placeholder, textarea::placeholder{
      color: #999;
      font-style: italic;
      font-family: Arial;
    }
  
    .subsection h2 {
      font-size: 20px;
      color: #666666;
      font-weight: 200;
    }
  
    #section {
      float: left;
    }
  
    .subsection div {
      font-size: 12px;
      color: #797979;
      line-height: 18px;
    }
  
    .question {
      span.check {
        float: left;
        margin-left: -31px;
        margin-top: 3px;
        background-color: green;
        border-radius: 21px;
        padding: 2px;
        color: white;
        width: 22px;
        text-align: center;
      }
      h1.title {
        font-size: 16px;
        color: #333;
        font-weight: 600;
      }
    
      .description {
        font-size: 12px;
        font-weight: 400;
        color: #666666;
        margin: 20px 0;
      }
    }
    .radio-group {
      margin-top: 20px;
      margin-bottom: 40px;
    }
    .question .radio-group .option {
      font-size: 18px;
      font-weight: 400;
      padding: 10px;
      padding-right: 20px;
      border-top-style: none;
      border-left-style: solid;
      border-bottom-style: none;
      border-right-style: none;
      border-left-color: #ff6600;
  
    }

    .option, .table tbody tr {
      td:first-of-type {
        border-top-style: none;
        border-left-width: 3px;
        border-left-style: solid;
        border-left-color: #ff6600;
      }
      td:last-of-type {
        display: inline-block;
      }
    }
    
    .question .radio-group .option:first-of-type {
      border-width: 3px;
    }
    .question .radio-group .option {
      border-width: 1px;
    }
  
    .guidance-page {
      float: left;
      width: 300px;
      margin-top: 40px;
      margin-left: 25px;
    }
  
    #content {
      margin-top: 95px;
      display: flex;
      flex-direction: column;
    }
  
    .question .table {
      table-layout: fixed;

      .table-add-button, .table-delete-button {
        float: right;
        margin-right: 5px;
        background-color: #0067b1;
        border-radius: 6px;
        color: #eee;
        border: none;
        padding: 5px 3px;
      }
    }
    
    td {
      vertical-align: top;
    }
  
    table {
      margin-bottom: 10px;
      td {
        border: 1px solid #eee;
      }
      textarea {
        width: 100%;
        padding: 0;
        margin: 0;
      }
    }
  
    textarea {
        border: none;
    }
  }
</style>
