<template>
    <header>
        <div class="logo pointer">
            <img src="../assets/avada-music-logo.png" alt="Logo">
        </div>
        <button class="menu-btn pointer" @click="$emit('open')">
            <i class="fa-solid fa-bars"></i>
        </button>
    </header>
    <div class="main">
        <h1>Untold Stories</h1>
        <h5><em>There is an untold story behind every favorite song.</em></h5>
        <div class="main-btns">
            <button class="main-btn red-btn pointer">
                LATEST ALBUM
            </button>
            <button class="main-btn transparent-btn pointer">
                LIVE DATES
            </button>
        </div>
    </div>
</template>

<style lang="scss">
    @use '../styles/variables' as *;

    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 20px;
        & .logo {
            & img {
                width: 180px;
                
            }
        }
    }

    .main {
        color: white;
        margin-top: 75px;
        text-align: center;
        & h1 {
            font-size: 70px;
            margin-bottom: 10px;
            letter-spacing: 1px;
        }
        & h5 {
            color: #fefefe;
            font-weight: 300;
        }
        & .main-btns {
            margin-top: 30px;
            & .main-btn {
                padding: 9px 17px;
                border: none;
                margin: 5px;
                color: white;
                font-size: 10px;
                letter-spacing: 1.4px;
                font-weight: 100;
            }
            & .transparent-btn {
                background-color: transparent;
                border: 1px solid white;
                &:hover {
                    background-color: #fefefe;
                    color: black;
                }
            }
        }
        
    }


</style>

<script>
    export default {
        name: 'Header'
    }
</script>