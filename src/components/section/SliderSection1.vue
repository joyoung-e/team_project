<template>
    <section id="sliderSection1" class="row">
        <h3 class="slide__title">국내 인기 여행지</h3>
        <div class="slide__inner">
            <swiper class="swiper" :options="swiperOption">
                <swiper-slide v-for="(slider, index) in sliders" :key="index">
                    <img 
                    :src="slider.currentImage" 
                    :alt="slider.alt" >
                    <div class="slide-text">
                        <p>{{  slider.title }}</p>
                    </div>
                </swiper-slide>
                <div class="swiper-button-prev" slot="button-prev"></div>
                <div class="swiper-button-next" slot="button-next"></div>
            </swiper>
        </div>
    </section>
</template>

<script>
    import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
    import '@/assets/css/myswiper.css'

    export default {
        name:"SliderSection1",
        components: {
            Swiper,
            SwiperSlide
        },
        data(){
            return {
                sliders : [
                    { currentImage:"src/assets/image/01.jpg", alt:"제주", title: '제주' },
                    { currentImage:"src/assets/image/02.jpg", alt:"서울", title: '서울' },
                    { currentImage:"src/assets/image/03.jpg", alt:"부산", title: '부산' },
                    { currentImage:"src/assets/image/04.jpg", alt:"경주", title: '경주' },
                    { currentImage:"src/assets/image/05.jpg", alt:"여수", title: '여수' },
                    { currentImage:"src/assets/image/06.jpg", alt:"가평", title: '가평' },
                    { currentImage:"src/assets/image/01.jpg", alt:"제주", title: '제주' },
                    { currentImage:"src/assets/image/02.jpg", alt:"서울", title: '서울' }
                ],
                swiperOption: {
                    slidesPerView: 5,
                    slidesPerGroup : 1,
                    spaceBetween: 50,
                    freemode:true,
                    loop: true,
                    navigation: {
                        nextEl: '.swiper-button-next',
                        prevEl: '.swiper-button-prev'
                    }
                }
            }
        },    
        }
    
</script>

<style lang="scss" scoped>
    #sliderSection1 { margin:100px auto; font-family: "Noto Sans KR", sans-serif;
        .slide__title { text-align: center; margin: 20px 0;}
        .slide__inner {
            padding:0 50px; overflow:hidden;
            .swiper {
                img { border-radius:20px; cursor:pointer; }
                p { text-align: center; margin-top: 10px; }
                }  
            }
        }
</style>