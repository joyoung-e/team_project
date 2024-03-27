<template>
    <section id="selection">
          <ul class="gallery">
        <li>
          <div class="headline">
            <h2 class="__title">여기</h2>
            <router-link to="" class="detail">숙소찾기</router-link>
          </div>
        </li>
        <li>
          <div class="headline2">
            <h2 class="__title">어때</h2>
            <router-link to="survey" class="detail">추천받기</router-link>
          </div>
        </li>
      </ul>
    </section>
</template>

<script>
export default {
 
};
</script>

<style>
.selection {
  line-height: 1.5em;
  margin: 0;
}
a {
  text-decoration: none;
}
.gallery {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  height: 90vh;
}
.gallery li {
  border-right: 5px solid #fff;
  flex: 1;
  transition: 0.5s;
  position: relative;
}
.__title {
  font-family: "YeogiEottae", sans-serif;
  color: rgb(209, 42, 42);
  font-size: 40px;
  font-weight: 300;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.detail {
  font-family: "Noto Sans KR", sans-serif;
   width:150px;
   height:50px;
   border-radius:25px;
   background:rgba(0,0,0,0.5);
   color:#fff;
   font-weight: bold;
   font-size:15px; 
   text-align:center;
   line-height:50px; 
   position:absolute;
   top: 55%;
   left:50%;
   transform:translateX(-50%); 
}
.detail:hover {
  background:#fff;
  color: #000;
}
.gallery li:last-child {
border-right: none;
}
.gallery li:nth-child(1) {
  background: url(/src/assets/image/1.jpg)no-repeat center center;
  background-size: 1400px auto;
}
.gallery li:nth-child(2) {
  background: url(/src/assets/image/2.jpg)no-repeat center center;
  background-size: 1400px auto;
}
.gallery:hover li {
  flex: 1;
  filter: grayscale(1);
}
.gallery li:hover {
flex: 3;
filter: grayscale(0);
}
.headline .headline2 {
  position: absolute;
  background: #000;
  color: #fff;
  text-align: center;
}
</style>
