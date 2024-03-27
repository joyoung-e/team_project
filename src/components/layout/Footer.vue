<template>
    <footer id="footer">
        <div class="row">
            <div class="customer__company">
                <div class="footer__customer">
                    <h2>고객센터</h2>
                    <div class="customer__time">
                    오전 9시 - 새벽 3시 운영
                    </div>
                    <div class="customer__contact">
                    <div class="telephone">
                        <i class="fa-solid fa-phone"></i> 1670-6250
                    </div>
                    <div class="kakaotalk">
                        <i class="fa-solid fa-comment"></i> 카카오 문의
                    </div>
                    </div>
                </div> 
                <div class="footer__company">
                    <div class="company__service">
                        <div class="company">
                            <h2>회사</h2>
                            <div class="company__info">
                                회사소개
                            </div>
                        </div>
                        <div class="service">
                            <h2>서비스</h2>
                            <ul class="service__contents">
                                <li>공지사항</li>
                                <li>자주 묻는 질문</li>
                                <li>기업 출장/복지 서비스 문의</li>
                            </ul>
                        </div>
                    </div>
                    <div class="benefit">
                        <h2>혜택</h2>
                        <ul class="benefit__contents">
                            <li>트립홀릭 혜택 안내</li>
                            <li>엘리트 혜택 안내</li>
                            <li>비즈니스 회원 혜택 안내</li>
                            <li>여기어때 상품권 조회</li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="address__law">
                <div class="footer__address">
                    <p>(주)여기어때컴퍼니</p>
                    <p>주소 : 서울특별시 강남구 봉은사로 479, 479타워 11층 | 대표이사 : 정명훈 | 사업자등록번호 : 742-86-00224사업자정보확인</p>
                    <p>전자우편주소 : help@goodchoice.kr | 통신판매번호 : 2017-서울강남-01779 | 관광사업자 등록번호 : 제1026-24호 | 전화번호 : 1670-6250 | 호스팅서비스제공자의 상호 표시 : (주)여기어때컴퍼니</p>
                    <p>(주)여기어때컴퍼니는 통신판매중개자로서 통신판매의 당사자가 아니며, 상품의 예약, 이용 및 환불 등과 관련한 의무와 책임은 각 판매자에게 있습니다.</p>
                </div>
                <div class="footer__law">
                    <ul class="laws">
                        <li>이용약관</li>
                        <li class="law__bold">개인정보처리방침</li>
                        <li>소비자 분쟁해결 기준</li>
                        <li>콘텐츠산업진흥법에 의한 표시</li>
                    </ul>
                    <span class="icon">
                        <span><a href="#"><i class="fa-brands fa-facebook"></i></a></span>
                        <span><a href="#"><i class="fa-brands fa-instagram"></i></a></span>
                    </span>
                </div>
            </div>
            <div class="copyright">
                Copyright GC COMPANY Corp. All rights reserved.
            </div>
        </div>
    </footer>
</template>

<script>
    export default {
        name: "Footer"
    }
</script>

<style lang="scss" scoped>
#footer {
    background: #fafafa;
    .row {
        padding: 40px 0 64px;
        display: flex;
        flex-direction: column;
        .customer__company{
            display: flex;
            border-bottom : 1px solid#000;
            border-color: rgba(245, 245, 245, 1);
            padding: 0 0 20px;
            .footer__customer {
                flex:1;
                display: flex;
                flex-direction: column;
                h2 {
                    margin: 0 0 16px;
                    font-size: 18px;
                    color: #707070;
                }
                .customer__time {
                    margin: 0 0 16px;
                    color: #999999;
                    font-size: 14px;
                    font-weight: 600;
                }
                .customer__contact {
                    display: flex;
                    .telephone {
                        border: 2px solid rgba(245, 245, 245, 1);
                        background: #fff;
                        border-radius: 10px;
                        width: 142px;
                        height: 48px;
                        display: flex;
                        justify-content: center;
                        align-items: center;
                        color: #333;
                    }
                    .kakaotalk {
                        border: 2px solid rgba(245, 245, 245, 1);
                        background: #fff;
                        border-radius: 10px;
                        width: 142px;
                        height: 48px;
                        display: flex;
                        justify-content: center;
                        align-items: center;
                        color: #333;
                    }
                }
            }
            .footer__company {
                flex:1;
                display: flex;
                gap: 24px;
                .company__service{
                    display: flex;
                    flex:1 60%;
                    .company{
                        flex:1;
                        display: flex;
                        flex-direction: column;
                        gap: 10px;
                        h2{
                            color:#707070;
                            font-size:15px;
                        }
                        .company__info {
                            color: #999999;
                            font-size: 14px;
                        }
                    }
                    .service{
                        flex:1;
                        display: flex;
                        flex-direction: column;
                        gap: 10px;
                        h2{
                            color:#707070;
                            font-size:15px;
                        }
                        .service__contents {
                            color: #999999;
                            font-size: 14px;
                            display: flex;
                            flex-direction: column;
                            li {
                                flex:1;
                                padding-bottom: 10px;
                            }
                        } 
                    }
                }
                .benefit {
                    flex:1 40%;
                    display: flex;
                    flex-direction: column;
                    gap: 10px;
                    h2{
                        color:#707070;
                        font-size:15px;
                    }
                    .benefit__contents {
                        color: #999999;
                        font-size: 14px;
                        li {
                            flex:1;
                            padding-bottom: 10px;
                        }
                    }
                }
            }
        }
        .address__law{
            .footer__address{
                font-size: 12px;
                color:#999999;
            }
            .footer__law {
                display: flex;
                justify-content: space-between;
                .laws {
                    flex: 1;
                    display: flex;
                    margin: 16px 0 32px;
                    font-size: 14px;
                    font-weight: 600;
                    gap: 16px;
                    color: #999999;
                    .law__bold {
                        color: #000;
                    }
                }
                .icon {
                    display: flex;
                    align-items: center;
                    gap: 10px;
                    i {
                        font-size: 30px;
                        color: #707070
                    }
                }
            }
        }
        .copyright {
            font-size:12px;
            color: #999999;
        }
    }
}
</style>