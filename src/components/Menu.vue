<template>
    <div class="menu">
        <div class="top-menu">
            <img src="../assets/avada-music-logo.png" alt="logo menu" class="pointer">
            <button class="pointer menu-btn" @click="$emit('closeMenu')">
                <i class="fa-solid fa-xmark"></i>
            </button>
        </div>
        <div class="body-menu">
            <ul>
                <li v-for="(link, index) in links" class="pointer" :class="index==0?'active':''">{{links[index]}}</li>
            </ul>
        </div>
    </div>
</template>


<style lang="scss">
@use '../styles/variables' as *;
    .menu {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        z-index: 12353;
        overflow: hidden;
        background-color: $red;
        & .top-menu {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px;
            & img {
                width: 180px;
            }
            & button {
                color: rgb(223, 223, 223);
            }
        }
        .body-menu {
            text-align: center;
            margin-top: 230px;
            & li {
                color: #f8959e;
                font-size: 30px;
                font-weight: 300;
                margin: 40px;
                &:hover {
                    color: white;
                }
            }
            
        }
    }
</style>

<script>
    export default {
        name: 'Menu',
        data() {
            return {
                links: [
                    'Home',
                    'Meet The Band',
                    'Live Dates',
                    'Latest News',
                    'Albums',
                    'Fans'
                ]
            }
        }
    }
</script>