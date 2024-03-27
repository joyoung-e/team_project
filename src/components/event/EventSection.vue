<template>
  <section id="EventSection">
    <h1>이벤트</h1>
        <p>#HOT &nbsp;&nbsp;#모텔 &nbsp;&nbsp;#호텔 &nbsp;&nbsp;#리조트 &nbsp;&nbsp;#펜션 &nbsp;&nbsp;#캠핑 &nbsp;&nbsp;#게스트하우스 &nbsp;&nbsp;#해외여행</p>
      <div class="event__list">
              <ul>
                  <li v-for="(item, index) in events" :key="index"  @click="showEventImage(item)">
                          <div>
                              <img :src="item.photo" :alt="item.title">
                              <span class="name">{{ item.title }}</span>
                              <span>{{ item.date }}</span>
                          </div>
                  </li>
              </ul>
      </div>
      <div v-if="selectedEvent" class="modal">
      <div class="modal-content">
        <span class="close" @click="closeModal">&times;</span>
        <h2>{{ selectedEvent.title }}</h2>
        <p>&nbsp;&nbsp;&nbsp;&nbsp;이벤트 자세히보기 → </p>
        <img :src="selectedEvent.img" :alt="selectedEvent.title" class="modal-image">
      </div>
    </div>
    
  </section>
</template>

<script>

  export default {
      name: "EventSection",
      data(){
          return {
              events : [
                  {
                    title: "봄맞이 국내여행 쿠폰세트",
                    date: "24.03.01 - 24.03.31",
                    photo: "/image/event_01.webp",
                    img: "src/assets/image/e_01.png"
                  },
                  {
                    title: "해외 봄꽃여행 쿠폰팩",
                    date: "24.03.01 - 24.03.31",
                    photo: "/image/event_02.webp",
                    img: "src/assets/image/e_02.jpg"
                },
                  {
                    title: "위클리 오픈런",
                    date: "24.03.01 - 24.03.31",
                    photo: "/image/event_03.webp",
                    img: "src/assets/image/e_03.png"
                  },
                  {
                      title:"베스트 호텔딜",
                      date:"24.03.01 - 24.03.31",
                      photo: "/image/event_04.webp",
                      img: "src/assets/image/e_04.jpg"
                  },
                  {
                      title:"인기 호텔 최대 5만원 할인",
                      date:"24.03.01 - 24.03.31",
                      photo: "/image/event_05.webp",
                      img: "/image/event_05.webp"
                  },
                  {
                      title:"반려견과 블랙어때",
                      date:"24.03.01 - 24.03.31",
                      photo: "/image/event_06.webp",
                      img: "src/assets/image/e_05.jpg"
                  },
                  {
                      title:"인기 펜션 최대 5만원 할인",
                      date:"24.03.01 - 24.03.31",
                      photo: "/image/event_07.webp",
                      img: "/image/event_07.webp"
                  },
                  {
                      title:"인기공간 할인파티",
                      date:"24.03.01 - 24.03.31",
                      photo: "/image/event_08.webp",
                      img: "src/assets/image/e_06.png"
                  },
                  {
                      title:"3월 신규회원 웰컴쿠폰",
                      date:"24.03.01 - 24.03.31",
                      photo: "/image/event_09.webp",
                      img: "src/assets/image/e_07.png"
                  },
                  {
                      title:"24년 3월 결제 프로모션 모음",
                      date:"24.03.01 - 24.03.31",
                      photo: "/image/event_10.webp",
                      img: "src/assets/image/e_08.png"
                  },
              ],
              selectedEvent: null           
          };
      },
      methods: {
    showEventImage(event) {
      this.selectedEvent = event;
    },
    closeModal() {
      this.selectedEvent = null;
    }
  }
};
</script>

<style lang="scss" scoped>
#EventSection {
  max-width: 1200px;
  margin: 50px auto;
  font-family: "Noto Sans KR", sans-serif;

  h1 {
    margin-top: 20px;
    font-size: 25px;
  }

  p {
    margin-top: 20px;
    font-size: 15px;
    color: #707070;
  }

  .event__list {
    margin: 10px 0;
    border-top: 1px solid #777777;

    ul {
      display: flex;
      flex-wrap: wrap;

      li {
        flex: 0 0 30%;
        margin: 40px 20px 10px;

        div {
          cursor: pointer;

          img {
            width: 100%;
            border-radius: 15px;
          }

          span {
            display: block;
            font-weight: bold;
            margin: 8px 0;
          }

          span:nth-child(3) {
            color: #666666;
            font-weight: 400;
          }
        }
      }
    }
  }
  .modal {
    display: block; 
    position: fixed;
    z-index: 1;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: hidden;
    background-color: rgba(0, 0, 0, 0.4); 
  }
  .modal-content {
    left: 0;
    top: -20%;
    background-color: #fefefe;
    margin: 15% auto;
    padding: 20px;
    width: 50%;
    position: relative;
}
.close {
    color: #aaa;
    float: right;
    font-size: 28px;
    font-weight: bold;
    position: absolute;
    top: 0;
    right: 0;
    margin-right: 20px;
    margin-top: 20px;
  }

  .close:hover,
  .close:focus {
    color: black;
    text-decoration: none;
    cursor: pointer;
  }

.modal-image {
  display: block;
  margin: 0px auto 30px;
  width: 50%;
  height: auto;
}
}
  
</style>