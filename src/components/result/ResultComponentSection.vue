<template>
    <section id="ResultComponentSection">
        <h1>
            <span>대한민국 1등 숙박 어플</span><br>
            <span class="title">여행할때 여기어때</span>
        </h1>
        <div class="travel__wrap">
            <div class="travel__type">
                <button :class="{active : activeButton==travelMenu.menu5 }" @click="handleClick(travelMenu.menu5)">{{ travelMenu.menu5 }}</button>
                <button :class="{active : activeButton==travelMenu.menu6 }" @click="handleClick(travelMenu.menu6)">{{ travelMenu.menu6 }}</button>
                <button :class="{active : activeButton==travelMenu.menu1 }" @click="handleClick(travelMenu.menu1)">{{ travelMenu.menu1 }}</button>
                <button :class="{active : activeButton==travelMenu.menu2 }" @click="handleClick(travelMenu.menu2)">{{ travelMenu.menu2 }}</button>
                <button :class="{active : activeButton==travelMenu.menu3 }" @click="handleClick(travelMenu.menu3)">{{ travelMenu.menu3 }}</button>
                <button :class="{active : activeButton==travelMenu.menu4 }" @click="handleClick(travelMenu.menu4)">{{ travelMenu.menu4 }}</button>
                <button :class="{active : activeButton==travelMenu.menu7 }" @click="handleClick(travelMenu.menu7)">{{ travelMenu.menu7 }}</button>
                <button :class="{active : activeButton==travelMenu.menu8 }" @click="handleClick(travelMenu.menu8)">{{ travelMenu.menu8 }}</button>
                <button :class="{active : activeButton==travelMenu.menu9 }" @click="handleClick(travelMenu.menu9)">{{ travelMenu.menu9 }}</button>
                <button :class="{active : activeButton==travelMenu.menu10 }" @click="handleClick(travelMenu.menu10)">{{ travelMenu.menu10 }}</button>
                <button :class="{active : activeButton==travelMenu.menu11 }" @click="handleClick(travelMenu.menu11)">{{ travelMenu.menu11 }}</button>
                
            </div>
            <div class="travel__member">                          
                <div class="member__info" v-for="(item, index) in activeTravel.travelInfo" :key="index">
                    <a :href="item.link">
                        <figure class="member__photo">
                            <img :src="item.travelImg" :alt="item.title">
                        </figure>
                        <div class="member__desc">
                            <h4>{{ item.title }}</h4>
                            <p>{{ item.data }}</p>
                            <span class="red">{{ item.data1 }}</span>
                            <span class="blue">{{ item.data2 }}</span>
                            <span class="gray">{{ item.data3 }}</span>
                        </div>
                    </a>
                </div>
            </div>
        </div>
        <h3>이번 주 블랙 PICK</h3>
        <h5>나를 위한 근사한 휴가, 여기어때 프리미엄 숙소</h5>
        <li>
            <div class="pick__photo">
                <a href="#"><img src="/image/pick_01.jpg" alt=""></a>
                <a href="#"><img src="/image/pick_02.jpg" alt=""></a>
                <a href="#"><img src="/image/pick_03.jpg" alt=""></a>
                <a href="#"><img src="/image/pick_04.jpg" alt=""></a>
            </div>
        </li>
    </section>
  </template>
  
  <script>
    export default {
        name:"ResultComponentSection",
        data(){
            return { 
                activeButton : '추천결과',
                travelMenu:{
                  menu1 : '호캉스',
                  menu2 : '힐링',
                  menu3 : '액티비티',
                  menu4 : '식도락',
                  menu5 : '추천결과',
                  menu6 : '해외', 
                  menu7 : '국내',
                  menu8 : '호텔',
                  menu9 : '펜션',
                  menu10 : '캠핑',
                  menu11 : '체험'
                },
                travelData:[
                    { 
                        menu : "추천결과",
                        travelInfo: [ 
                            { travelImg : "src/assets/image/01.jpg", title:"제주", data:"제주롯데호텔", data1:"블랙·5성급·호텔", data2:"리조트", data3:"서귀포시", link:"#" },
                            { travelImg : "src/assets/image/_05.jpg", title:"다낭", data:"살라 다낭 비치", data1:"4.5등급·호텔", data2:"리조트", data3:"프억 미",  link:"#" },
                            { travelImg : "src/assets/image/_06.jpg", title:"괌", data:"두짓타니 괌 리조트", data1:"4등급·호텔", data2:"리조트", data3:"투몬 베이", link:"#" },
                            { travelImg : "src/assets/image/03.jpg", title:"부산", data:"해운대 동백호텔", data1:"모텔", data2:"호텔", data3:"해운대역", link:"#" },
                            { travelImg : "src/assets/image/08.jpg", title:"속초", data:"라마다 속초", data1:"특급·호텔", data2:"리조트", data3:"속초시", link:"#" },
                            { travelImg : "src/assets/image/04.jpg", title:"경주", data:"힐튼경주", data1:"블랙·5성급·호텔", data2:"리조트", data3:"경주시", link:"#" },
                            { travelImg : "src/assets/image/_07.jpg", title:"싱가폴", data:"힐튼 싱가폴 오챠드", data1:"5등급·호텔", data2:"리조트", data3:"오차드", link:"#" },
                            { travelImg : "src/assets/image/02.jpg", title:"서울", data:"종로 부티크 호텔K", data1:"모텔", data2:"호텔", data3:"종로3가역", link:"#" },  
                        ]
                    },
                    { 
                        menu : "호캉스",
                        travelInfo: [ 
                            { travelImg : "src/assets/image/_03.jpg", title:"나트랑", data:"리게일리어 골드 호텔", data1:"5등급·호텔", data2:"리조트", data3:"떤럽",  link:"#" },
                            { travelImg : "src/assets/image/_05.jpg", title:"다낭", data:"살라 다낭 비치", data1:"4.5등급·호텔", data2:"리조트", data3:"프억 미",  link:"#" },
                            { travelImg : "src/assets/image/_06.jpg", title:"괌", data:"두짓타니 괌 리조트", data1:"4등급·호텔", data2:"리조트", data3:"투몬 베이",  link:"#" },
                            { travelImg : "src/assets/image/01.jpg", title:"제주", data:"제주신라호텔", data1:"블랙·5성급·호텔", data2:"리조트", data3:"서귀포시", link:"#" },
                            { travelImg : "src/assets/image/02.jpg", title:"서울", data:"종로 부티크 호텔K", data1:"모텔", data2:"호텔", data3:"종로3가역", link:"#" },
                            { travelImg : "src/assets/image/03.jpg", title:"부산", data:"해운대 동백호텔", data1:"모텔", data2:"호텔", data3:"해운대역", link:"#" },
                            { travelImg : "src/assets/image/_07.jpg", title:"싱가폴", data:"힐튼 싱가폴 오챠드", data1:"5등급·호텔", data2:"리조트", data3:"오차드", link:"#" },
                            { travelImg : "src/assets/image/_08.jpg", title:"코타키나발루", data:"코타 키나발루 메리어트 호텔", data1:"5등급·호텔", data2:"리조트", data3:"중심 업무 지구", link:"#" },
                            { travelImg : "src/assets/image/_03.jpg", title:"나트랑", data:"버고호텔", data1:"5등급·호텔", data2:"리조트", data3:"떤럽", link:"#" },
                            { travelImg : "src/assets/image/_05.jpg", title:"다낭", data:"해운대 동백호텔", data1:"모텔", data2:"호텔", data3:"해운대역", link:"#" },
                            { travelImg : "src/assets/image/_06.jpg", title:"괌", data:"두짓타니 괌 리조트", data1:"4등급·호텔", data2:"리조트", data3:"투몬 베이", link:"#" },
                            { travelImg : "src/assets/image/01.jpg", title:"제주", data:"제주신라호텔", data1:"블랙·5성급·호텔", data2:"리조트", data3:"서귀포시", link:"#" },
                            { travelImg : "src/assets/image/02.jpg", title:"서울", data:"종로 부티크 호텔K", data1:"모텔", data2:"호텔", data3:"종로3가역", link:"#" },
                            { travelImg : "src/assets/image/03.jpg", title:"부산", data:"해운대 동백호텔", data1:"모텔", data2:"호텔", data3:"해운대역", link:"#" },
                            { travelImg : "src/assets/image/_07.jpg", title:"싱가폴", data:"힐튼 싱가폴 오챠드", data1:"5등급·호텔", data2:"리조트", data3:"오차드", link:"#" },
                            { travelImg : "src/assets/image/_08.jpg", title:"코타키나발루", data:"코타 키나발루 메리어트 호텔", data1:"5등급·호텔", data2:"리조트", data3:"중심 업무 지구", link:"#" },
                          
                        ]
                    },
                    { 
                        menu : "힐링",
                        travelInfo: [ 
                            { travelImg : "src/assets/image/01.jpg", title:"제주", data:"제주신라호텔", data1:"블랙·5성급·호텔", data2:"리조트", data3:"서귀포시", link:"#" },
                            { travelImg : "src/assets/image/04.jpg", title:"경주", data:"힐튼경주", data1:"블랙·5성급·호텔", data2:"리조트", data3:"경주시", link:"#" },
                            { travelImg : "src/assets/image/03.jpg", title:"부산", data:"해운대 동백호텔", data1:"모텔", data2:"호텔", data3:"해운대역", link:"#" },
                            { travelImg : "src/assets/image/_03.jpg", title:"나트랑", data:"앨마 리조트 깜라인", data1:"4등급·호텔", data2:"깜하이동", data3:"떤럽", link:"#" },
                            { travelImg : "src/assets/image/_05.jpg", title:"다낭", data:"해운대 동백호텔", data1:"모텔", data2:"호텔", data3:"해운대역", link:"#" },
                            { travelImg : "src/assets/image/_06.jpg", title:"괌", data:"두짓타니 괌 리조트", data1:"4등급·호텔", data2:"리조트", data3:"투몬 베이", link:"#" },
                            { travelImg : "src/assets/image/_04.jpg", title:"후쿠오카", data:"미츠이 가든 호텔 후투오카 나카스", data1:"4등급·호텔", data2:"리조트", data3:"하카타", link:"#" },
                            { travelImg : "src/assets/image/_08.jpg", title:"코타키나발루", data:"코타 키나발루 메리어트 호텔", data1:"5등급·호텔", data2:"리조트", data3:"중심 업무 지구", link:"#" },
                            { travelImg : "src/assets/image/01.jpg", title:"제주", data:"제주신라호텔", data1:"블랙·5성급·호텔", data2:"리조트", data3:"서귀포시", link:"#" },
                            { travelImg : "src/assets/image/04.jpg", title:"경주", data:"힐튼경주", data1:"블랙·5성급·호텔", data2:"리조트", data3:"경주시", link:"#" },
                            { travelImg : "src/assets/image/03.jpg", title:"부산", data:"해운대 동백호텔", data1:"모텔", data2:"호텔", data3:"해운대역", link:"#" },
                            { travelImg : "src/assets/image/_03.jpg", title:"나트랑", data:"버고호텔", data1:"5등급·호텔", data2:"리조트", data3:"떤럽", link:"#" },
                            { travelImg : "src/assets/image/_05.jpg", title:"다낭", data:"해운대 동백호텔", data1:"모텔", data2:"호텔", data3:"해운대역", link:"#" },
                            { travelImg : "src/assets/image/_06.jpg", title:"괌", data:"두짓타니 괌 리조트", data1:"4등급·호텔", data2:"리조트", data3:"투몬 베이", link:"#" },
                            { travelImg : "src/assets/image/_04.jpg", title:"후쿠오카", data:"미츠이 가든 호텔 후투오카 나카스", data1:"4등급·호텔", data2:"리조트", data3:"하카타", link:"#" },
                            { travelImg : "src/assets/image/_08.jpg", title:"코타키나발루", data:"코타 키나발루 메리어트 호텔", data1:"5등급·호텔", data2:"리조트", data3:"중심 업무 지구", link:"#" },
                           
                        ]
                    },
                    { 
                        menu : "액티비티",
                        travelInfo: [ 
                            { travelImg : "src/assets/image/01.jpg", title:"제주", data:"제주신라호텔", data1:"블랙·5성급·호텔", data2:"리조트", data3:"서귀포시", link:"#" },
                            { travelImg : "src/assets/image/_09.jpg", title:"방콕", data:"차트리움 그랜드 방콕", data1:"5등급·호텔", data2:"리조트", data3:"시암", link:"#" },
                            { travelImg : "src/assets/image/03.jpg", title:"부산", data:"해운대 동백호텔", data1:"모텔", data2:"호텔", data3:"해운대역", link:"#" },
                            { travelImg : "src/assets/image/_03.jpg", title:"나트랑", data:"버고호텔", data1:"5등급·호텔", data2:"리조트", data3:"떤럽", link:"#" },
                            { travelImg : "src/assets/image/08.jpg", title:"속초", data:"라마다 속초", data1:"특급·호텔", data2:"리조트", data3:"속초시", link:"#" },
                            { travelImg : "src/assets/image/_06.jpg", title:"괌", data:"두짓타니 괌 리조트", data1:"4등급·호텔", data2:"리조트", data3:"투몬 베이", link:"#" },
                            { travelImg : "src/assets/image/07.jpg", title:"가평", data:"가평 디프라이빗 캠핑", data1:"캠핑", data2:"펜션", data3:"가평군", link:"#" },
                            { travelImg : "src/assets/image/05.jpg", title:"여수", data:"신라스테이 여수", data1:"호텔", data2:"비즈니스", data3:"여수시", link:"#" },
                            { travelImg : "src/assets/image/01.jpg", title:"제주", data:"제주신라호텔", data1:"블랙·5성급·호텔", data2:"리조트", data3:"서귀포시", link:"#" },
                            { travelImg : "src/assets/image/_09.jpg", title:"방콕", data:"차트리움 그랜드 방콕", data1:"5등급·호텔", data2:"리조트", data3:"시암", link:"#" },
                            { travelImg : "src/assets/image/03.jpg", title:"부산", data:"해운대 동백호텔", data1:"모텔", data2:"호텔", data3:"해운대역", link:"#" },
                            { travelImg : "src/assets/image/_03.jpg", title:"나트랑", data:"버고호텔", data1:"5등급·호텔", data2:"리조트", data3:"떤럽", link:"#" },
                            { travelImg : "src/assets/image/08.jpg", title:"속초", data:"라마다 속초", data1:"특급·호텔", data2:"리조트", data3:"속초시", link:"#" },
                            { travelImg : "src/assets/image/_06.jpg", title:"괌", data:"두짓타니 괌 리조트", data1:"4등급·호텔", data2:"리조트", data3:"투몬 베이", link:"#" },
                            { travelImg : "src/assets/image/07.jpg", title:"가평", data:"가평 디프라이빗 캠핑", data1:"캠핑", data2:"펜션", data3:"가평군", link:"#" },
                            { travelImg : "src/assets/image/05.jpg", title:"여수", data:"신라스테이 여수", data1:"호텔", data2:"비즈니스", data3:"여수시", link:"#" },
                           
                        ]
                    },
                    { 
                        menu : "식도락",
                        travelInfo: [ 
                            { travelImg : "src/assets/image/05.jpg", title:"여수", data:"신라스테이 여수", data1:"호텔", data2:"비즈니스", data3:"여수시", link:"#" },
                            { travelImg : "src/assets/image/_09.jpg", title:"방콕", data:"차트리움 그랜드 방콕", data1:"5등급·호텔", data2:"리조트", data3:"시암", link:"#" },
                            { travelImg : "src/assets/image/03.jpg", title:"부산", data:"해운대 동백호텔", data1:"모텔", data2:"호텔", data3:"해운대역", link:"#" },
                            { travelImg : "src/assets/image/08.jpg", title:"속초", data:"라마다 속초", data1:"특급·호텔", data2:"리조트", data3:"속초시", link:"#" },
                            { travelImg : "src/assets/image/04.jpg", title:"경주", data:"힐튼경주", data1:"블랙·5성급·호텔", data2:"리조트", data3:"경주시", link:"#" },
                            { travelImg : "src/assets/image/02.jpg", title:"서울", data:"종로 부티크 호텔K", data1:"모텔", data2:"호텔", data3:"종로3가역", link:"#" },
                            { travelImg : "src/assets/image/_04.jpg", title:"후쿠오카", data:"미츠이 가든 호텔 후투오카 나카스", data1:"4등급·호텔", data2:"리조트", data3:"하카타", link:"#" },
                            { travelImg : "src/assets/image/10.jpg", title:"제주도", data:"제주신라호텔", data1:"블랙·5성급·호텔", data2:"리조트", data3:"서귀포시", link:"#" },
                            { travelImg : "src/assets/image/05.jpg", title:"여수", data:"신라스테이 여수", data1:"호텔", data2:"비즈니스", data3:"여수시", link:"#" },
                            { travelImg : "src/assets/image/_09.jpg", title:"방콕", data:"차트리움 그랜드 방콕", data1:"5등급·호텔", data2:"리조트", data3:"시암", link:"#" },
                            { travelImg : "src/assets/image/03.jpg", title:"부산", data:"해운대 동백호텔", data1:"모텔", data2:"호텔", data3:"해운대역", link:"#" },
                            { travelImg : "src/assets/image/08.jpg", title:"속초", data:"라마다 속초", data1:"특급·호텔", data2:"리조트", data3:"속초시", link:"#" },
                            { travelImg : "src/assets/image/04.jpg", title:"경주", data:"힐튼경주", data1:"블랙·5성급·호텔", data2:"리조트", data3:"경주시", link:"#" },
                            { travelImg : "src/assets/image/02.jpg", title:"서울", data:"종로 부티크 호텔K", data1:"모텔", data2:"호텔", data3:"종로3가역", link:"#" },
                            { travelImg : "src/assets/image/_04.jpg", title:"후쿠오카", data:"미츠이 가든 호텔 후투오카 나카스", data1:"4등급·호텔", data2:"리조트", data3:"하카타", link:"#" },
                            { travelImg : "src/assets/image/10.jpg", title:"제주도", data:"제주신라호텔", data1:"블랙·5성급·호텔", data2:"리조트", data3:"서귀포시", link:"#" },
                        ]
                    },
                    { 
                        menu : "국내",
                        travelInfo: [ 
                            { travelImg : "src/assets/image/01.jpg", title:"제주", data:"제주롯데호텔", data1:"블랙·5성급·호텔", data2:"리조트", data3:"서귀포시", link:"#" },
                            { travelImg : "src/assets/image/07.jpg", title:"가평", data:"가평 디프라이빗 캠핑", data1:"캠핑", data2:"펜션", data3:"가평군", link:"#" },
                            { travelImg : "src/assets/image/05.jpg", title:"여수", data:"신라스테이 여수", data1:"호텔", data2:"비즈니스", data3:"여수시", link:"#" },
                            { travelImg : "src/assets/image/03.jpg", title:"부산", data:"해운대 동백호텔", data1:"모텔", data2:"호텔", data3:"해운대역", link:"#" },
                            { travelImg : "src/assets/image/08.jpg", title:"속초", data:"라마다 속초", data1:"특급·호텔", data2:"리조트", data3:"속초시", link:"#" },
                            { travelImg : "src/assets/image/04.jpg", title:"경주", data:"힐튼경주", data1:"블랙·5성급·호텔", data2:"리조트", data3:"경주시", link:"#" },
                            { travelImg : "src/assets/image/02.jpg", title:"서울", data:"종로 부티크 호텔K", data1:"모텔", data2:"호텔", data3:"종로3가역", link:"#" },
                            { travelImg : "src/assets/image/10.jpg", title:"제주도", data:"제주신라호텔", data1:"블랙·5성급·호텔", data2:"리조트", data3:"서귀포시", link:"#" },
                            
                            
                        ]
                    },
                    { 
                        menu : "해외",
                        travelInfo: [ 
                            { travelImg : "src/assets/image/_04.jpg", title:"후쿠오카", data:"미츠이 가든 호텔 후투오카 나카스", data1:"4등급·호텔", data2:"리조트", data3:"하카타", link:"#" },
                            { travelImg : "src/assets/image/_03.jpg", title:"나트랑", data:"버고호텔", data1:"5등급·호텔", data2:"리조트", data3:"떤럽", link:"#" },
                            { travelImg : "src/assets/image/_05.jpg", title:"다낭", data:"해운대 동백호텔", data1:"모텔", data2:"호텔", data3:"해운대역", link:"#" },
                            { travelImg : "src/assets/image/_06.jpg", title:"괌", data:"두짓타니 괌 리조트", data1:"4등급·호텔", data2:"리조트", data3:"투몬 베이", link:"#" },
                            { travelImg : "src/assets/image/_07.jpg", title:"싱가폴", data:"힐튼 싱가폴 오챠드", data1:"5등급·호텔", data2:"리조트", data3:"오차드", link:"#" },
                            { travelImg : "src/assets/image/_08.jpg", title:"코타키나발루", data:"코타 키나발루 메리어트 호텔", data1:"5등급·호텔", data2:"리조트", data3:"중심 업무 지구", link:"#" },
                            { travelImg : "src/assets/image/_03.jpg", title:"나트랑", data:"버고호텔", data1:"5등급·호텔", data2:"리조트", data3:"떤럽", link:"#" },
                            { travelImg : "src/assets/image/_05.jpg", title:"다낭", data:"해운대 동백호텔", data1:"모텔", data2:"호텔", data3:"해운대역", link:"#" },
                            { travelImg : "src/assets/image/_06.jpg", title:"괌", data:"두짓타니 괌 리조트", data1:"4등급·호텔", data2:"리조트", data3:"투몬 베이", link:"#" },
                            { travelImg : "src/assets/image/_07.jpg", title:"싱가폴", data:"힐튼 싱가폴 오챠드", data1:"5등급·호텔", data2:"리조트", data3:"오차드", link:"#" },
                            { travelImg : "src/assets/image/_08.jpg", title:"코타키나발루", data:"코타 키나발루 메리어트 호텔", data1:"5등급·호텔", data2:"리조트", data3:"중심 업무 지구", link:"#" },
                            { travelImg : "src/assets/image/_04.jpg", title:"후쿠오카", data:"미츠이 가든 호텔 후투오카 나카스", data1:"4등급·호텔", data2:"리조트", data3:"하카타", link:"#" },
                        ]
                    },
                    { 
                        menu : "호텔",
                        travelInfo: [ 
                            { travelImg : "src/assets/image/02.jpg", title:"서울", data:"종로 부티크 호텔K", data1:"모텔", data2:"호텔", data3:"종로3가역", link:"#" },     
                            { travelImg : "src/assets/image/01.jpg", title:"제주", data:"제주롯데호텔", data1:"블랙·5성급·호텔", data2:"리조트", data3:"서귀포시", link:"#" },
                            { travelImg : "src/assets/image/_05.jpg", title:"다낭", data:"살라 다낭 비치", data1:"4.5등급·호텔", data2:"리조트", data3:"프억 미",  link:"#" },
                            { travelImg : "src/assets/image/_06.jpg", title:"괌", data:"두짓타니 괌 리조트", data1:"4등급·호텔", data2:"리조트", data3:"투몬 베이", link:"#" },
                            { travelImg : "src/assets/image/03.jpg", title:"부산", data:"해운대 동백호텔", data1:"모텔", data2:"호텔", data3:"해운대역", link:"#" },
                            { travelImg : "src/assets/image/08.jpg", title:"속초", data:"라마다 속초", data1:"특급·호텔", data2:"리조트", data3:"속초시", link:"#" },
                            { travelImg : "src/assets/image/_07.jpg", title:"싱가폴", data:"힐튼 싱가폴 오챠드", data1:"5등급·호텔", data2:"리조트", data3:"오차드", link:"#" }, 
                        ]
                    },
                    { 
                        menu : "펜션",
                        travelInfo: [ 
                            { travelImg : "src/assets/image/03.jpg", title:"부산", data:"해운대 동백호텔", data1:"모텔", data2:"호텔", data3:"해운대역", link:"#" },
                            { travelImg : "src/assets/image/08.jpg", title:"속초", data:"라마다 속초", data1:"특급·호텔", data2:"리조트", data3:"속초시", link:"#" },
                            { travelImg : "src/assets/image/04.jpg", title:"경주", data:"힐튼경주", data1:"블랙·5성급·호텔", data2:"리조트", data3:"경주시", link:"#" },
                            { travelImg : "src/assets/image/01.jpg", title:"제주", data:"제주롯데호텔", data1:"블랙·5성급·호텔", data2:"리조트", data3:"서귀포시", link:"#" },
                            { travelImg : "src/assets/image/_05.jpg", title:"다낭", data:"살라 다낭 비치", data1:"4.5등급·호텔", data2:"리조트", data3:"프억 미",  link:"#" },
                            { travelImg : "src/assets/image/_06.jpg", title:"괌", data:"두짓타니 괌 리조트", data1:"4등급·호텔", data2:"리조트", data3:"투몬 베이", link:"#" },
                        ]
                    },
                    { 
                        menu : "캠핑",
                        travelInfo: [ 
                            { travelImg : "src/assets/image/08.jpg", title:"속초", data:"라마다 속초", data1:"특급·호텔", data2:"리조트", data3:"속초시", link:"#" },
                            { travelImg : "src/assets/image/01.jpg", title:"제주", data:"제주롯데호텔", data1:"블랙·5성급·호텔", data2:"리조트", data3:"서귀포시", link:"#" },
                            { travelImg : "src/assets/image/04.jpg", title:"경주", data:"힐튼경주", data1:"블랙·5성급·호텔", data2:"리조트", data3:"경주시", link:"#" },
                        ]
                    },
                    { 
                        menu : "체험",
                        travelInfo: [ 
                            { travelImg : "src/assets/image/_06.jpg", title:"괌", data:"두짓타니 괌 리조트", data1:"4등급·호텔", data2:"리조트", data3:"투몬 베이", link:"#" },
                            { travelImg : "src/assets/image/08.jpg", title:"속초", data:"라마다 속초", data1:"특급·호텔", data2:"리조트", data3:"속초시", link:"#" },
                            { travelImg : "src/assets/image/02.jpg", title:"서울", data:"종로 부티크 호텔K", data1:"모텔", data2:"호텔", data3:"종로3가역", link:"#" },
                            { travelImg : "src/assets/image/01.jpg", title:"제주", data:"제주롯데호텔", data1:"블랙·5성급·호텔", data2:"리조트", data3:"서귀포시", link:"#" },
                            { travelImg : "src/assets/image/_05.jpg", title:"다낭", data:"살라 다낭 비치", data1:"4.5등급·호텔", data2:"리조트", data3:"프억 미",  link:"#" },  
                        ]
                    },
                ]
            }
        },
        computed:{
            activeTravel() {
                return this.travelData.find((item)=> item.menu == this.activeButton  )
            }
        },
        methods : {
            handleClick(menu){
                this.activeButton = menu
            }
        },
  
    }
  </script>
  
  <style lang="scss" scoped>
    #ResultComponentSection {
        max-width:1200px;
        margin:50px auto;
        h1 {
            text-align: center;
            color: #3d3d3d;
            font-size: 25px;
            font-weight: 300;
            font-family: 'YeogiEottae', serif;
            .title {
                color: #f00;
                font-size: 50px;
                font-weight: 400;
                font-family: 'YeogiEottae', serif;
                display: inline-block;
                opacity: 0;
                animation: fadeIn 3s forwards;
                margin: 20px 0 60px 0 ;
            }
            @keyframes fadeIn {
                from {
                    opacity: 0;
                }
                to {
                    opacity: 1;
                }
            }
        }
        h3 { 
            font-family: "Noto Sans KR", sans-serif;
            border-top:1px solid #ddd;
            font-size:20px;
            font-weight: bold;
            color: #333;
            margin:50px 0 5px 20px;
            padding-top: 10px ;
        }
        h5 {
            font-family: "Noto Sans KR", sans-serif;
            font-size:17px;
            font-weight: 500;
            color: #646464;
            margin:0 0 10px 20px;
        }
        li {
            list-style-type: none;
            margin:0 20px 50px 10px ;
            .pick__photo {
                display: flex;
            // flex-wrap: wrap;
            a {
                flex: 1;
                margin:10px;
            }
        }
        }
        .travel__wrap {
            .travel__type { 
                display:flex;
                justify-content:center; 
                button { 
                    width: 80px;
                    font-size: 15px;
                    margin:0 15px 10px 0;
                    padding:10px ; 
                    border-radius:15px; 
                    transition:all 0.5s;
                    background: #fff;
                    border: 1px solid rgba($color: #ddd, $alpha: 0.5);
                    &.active { 
                        background:rgb(53, 147, 255); 
                        color:#fff }
                }
            }
            .travel__member { 
                display:flex; 
                flex-wrap:wrap;
                font-family: "Noto Sans KR", sans-serif;
                .member__info { 
                    flex:0 0 21%; 
                    margin:20px; 
                    a { 
                        display:block; 
                        .member__photo { 
                            img { 
                                width:100%; 
                                border-radius: 20px;
                                opacity: 1;
                            }
                            img:hover { 
                               opacity: 0.5;
                            }
                        }
                        .member__desc {
                            text-align: right;
                            h4 {
                                text-align: left;
                                margin: 10px 0 10px 10px;
                                font-size: 18px;
                                color: #555555;
                            }
                            p {
                                margin:0 5px 6px 0;
                                color: #3b3b3b;
                                font-size: 14px;
                                font-weight: 600;
                            }
                            .red {
                                font-size: 12px;
                                border-radius: 8px;
                                margin: 0 3px;
                                padding: 3px 5px;
                                background: rgb(255, 84, 54);
                                color: #fff;
                            }
                            .blue {
                                font-size: 12px;
                                border-radius: 8px;
                                margin: 0 3px;
                                padding: 3px 5px;
                                background: skyblue;
                                color: #fff;
                            }
                            .gray {
                                font-size: 12px;
                                border-radius: 8px;
                                margin: 0 3px;
                                padding: 3px 5px;
                                background: gray;
                                color: #fff;
                            }
                        }
                    }
                }
            }
        }
    }
  </style>