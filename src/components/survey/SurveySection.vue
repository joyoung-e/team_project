<template>
    <section id="surveySection">
      <h1>취향을 통해 나의 여행지를 찾아보세요!</h1>
      <form @submit.prevent="submitSurvey">
        <div v-for="(question, index) in questions" :key="index" class="question">
          <p class="question-text">{{ question.questionText }}</p>
          <div v-if="question.type === 'text'">
            <input type="text" v-model="responses[index]" />
          </div>
          
          <div v-else-if="question.type === 'radio'" class="options">
            <div v-for="(option, optionIndex) in question.options" :key="optionIndex" class="option">
                <input type="radio" :value="option" v-model="responses[index]" />
                <label class="option-label">{{ option }}</label>
            </div>
          </div>
        </div>
        <button type="submit">GO →</button>
      </form>
    </section>
  </template>
  
  <script>
  export default {
    data() {
      return {
        questions: [
          {
            questionText: "여행을 계획할때 주로 어떤 종류의 여행을 선호하시나요?",
            type: "radio",
            options: ["도시", "자연", "문화체험", "모험"]
          },
          {
            questionText: "여행지를 선택할때 어떤 종류의 숙박 시설을 선호하시나요?",
            type: "radio",
            options: ["호텔", "리조트", "캠핑", "에어비엔비", "펜션",]
          },
          {
            questionText: "여행을 할 때 가장 중요하게 고려하는 요소는 무엇인가요?",
            type: "radio",
            options: ["예산", "편의시설", "안전·보안", "현지 문화 경험", ]
          },
          {
            questionText: "이번 여행의 스타일을 선택해주세요.",
            type: "radio",
            options: ["호캉스", "힐링", "액티비티", "식도락"]
          }
        
        ],
        responses: []
      };
    },
    methods: {
      submitSurvey() {
        console.log("응답:", this.responses);
        this.$router.push('/result')
      }
    }
  };
  </script>
  
  <style lang="scss" scoped>
  #surveySection {
        max-width: 1200px;
        margin: 20px auto 0;
        padding:  50px 50px 80px 50px ;
        text-align: center;
        position: relative;
        background: rgb(223, 62, 62);
        h1 {
          font-size: 40px;
          font-weight: 100;
          font-family: 'YeogiEottae', serif;
          margin:0 150px 20px ;
          color:  rgb(223, 62, 62);
          background: #fff;
          padding: 20px 0;
          border-radius: 50px;
        }
          .question {
            padding: 30px 0 10px 0;
              .question-text {
                  font-weight: bold;
                  font-family: "Noto Sans KR", sans-serif;
                  background: #fff;
                  color:  rgb(223, 62, 62);
                  padding: 10px;
                  border-radius: 50px;
                  margin:0 320px 20px;
                }
                .options {
                  font-family: "Noto Sans KR", sans-serif;
                  display: flex;
                  flex-direction: row;
                  justify-content: center;
                  color: #fff;
                  .option {
                    margin-right: 20px;
 
                  }
                }
            }
            button {
              display: flex;
              justify-content:center;
              position: absolute;
              top: 94%;
              left: 50%;
              transform: translate(-50%, -50%);
              padding: 10px 20px;
              background-color: #fff;
              color: rgb(223, 62, 62);
              font-family: 'YeogiEottae', serif;
              border-radius: 30px;
              border: 1px solid #fff;
              cursor: pointer;
              font-size: 17px;
            }
            button:hover {
              background-color: rgb(223, 62, 62);
              color: #fff;

            }
          }
      
  
  </style>