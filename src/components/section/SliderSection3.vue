<template>
    <section id="sliderSection3">
        <h3 class="slide__title">이벤트</h3>
        <div class="slide__inner">
            <swiper class="swiper" :options="swiperOption">
                <swiper-slide v-for="(slider, index) in sliders" :key="index">
                    <img :src="slider.image" :alt="slider.alt">
                    <!-- <router-link :to="slider.href" class="detail"></router-link> -->
                </swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>
            </swiper>
        </div>
    </section>
</template>

<script>
    import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
    import '@/assets/css/myswiper.css'

    export default {
        name:"SliderSection3",
        components: {
            Swiper,
            SwiperSlide
        },
        data(){
            return {
                sliders : [
                    { image:"src/assets/image/event_01.webp", alt:"이미지1" },
                    { image:"src/assets/image/event_02.webp", alt:"이미지2" },
                    { image:"src/assets/image/event_03.webp", alt:"이미지3" },
                    { image:"src/assets/image/event_04.webp", alt:"이미지4" },
                    { image:"src/assets/image/event_05.webp", alt:"이미지5" },
                    { image:"src/assets/image/event_06.webp", alt:"이미지6" }
                ],
                swiperOption: {
                    slidesPerView: 3,
                    spaceBetween: 20,
                    effect:"slide",  // slide, cube, coverflow, flip
                    autoplay:{
                        delay:1000
                    },
                    loop: true,
                    pagination: {
                        el: '.swiper-pagination',
                        clickable: true
                    },
                    // navigation: {
                    //     nextEl: '.swiper-button-next',
                    //     prevEl: '.swiper-button-prev'
                    // }
                }
            }
        },
    }
</script>

<style lang="scss" scoped>
     #sliderSection3 { 
        max-width: 1200px ; margin:100px auto; font-family: "Noto Sans KR", sans-serif;
        .slide__title { text-align: center; margin: 20px 0;}
        .slide__inner {
            overflow:hidden;
            .swiper {
                img { border-radius:10px; cursor:pointer; ;}
                p {text-align: center; margin-top: 10px; }
                }  
            }
        }
        // .detail {
        //     width:200px; height:50px; border-radius:25px;
        //     background:rgba(0,0,0,0.5);
        //     color:#fff; font-size:20px; 
        //     text-align:center;
        //     line-height:50px; 
        //     position:absolute; bottom:100px; 
        //     left:50%; transform:translateX(-50%)
        //  }
    
</style>