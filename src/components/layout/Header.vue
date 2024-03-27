<template>
    <header id="header" class="row">
        <h1>
            <router-link to="/"><img src="../../assets/image/logo_px.png" alt=""></router-link>
        </h1>
        <nav class="header__nav">
            <div class="event">
                <router-link to="/event">이벤트</router-link>
            </div>
            <div class="customer">
                <router-link to="/customer">고객센터</router-link>
            </div>
            <div class="menu">
                <div class="bar">
                    <i class="fa-solid fa-bars"></i>
                </div>
                <div class="profile">
                    <i class="fa-solid fa-user"></i>
                </div>
            </div>
            <div class="menu__contents">
                <ul>
                    <li>
                        로그인/회원가입
                    </li>
                    <li>
                        비회원 예약조회
                    </li>
                </ul>
            </div>
        </nav>
    </header>
</template>

<script>
import axios from 'axios';
    export default {
        name: "Header"
    }
</script>

<style lang="scss" scoped>
    #header {
        height: 75px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        h1 {
            width: 110px;
            a {
                display: block;
            }
        }
        .header__nav {
            width: 252.8px;
            height: 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            text-align: center;
            gap: 16px;
            .event{
                flex:1;
            }
            .customer{
                flex:1;
            }
            .menu {
                position: relative;
                width: 76px;
                height: 40px;
                display: flex;
                align-items: center;
                gap: 6px;
                border-radius: 9999px;
                border: 1px solid #000;
                padding: 0 13px;
                .bar{
                    flex: 1;
                }
                .profile{
                    flex:1;
                }
            }
            .menu__contents {
                width: 168px;
                height: 88px;
                display: none;
                position: absolute;
                top: 10px;
                left: 0;
            }
        }
    }
</style>