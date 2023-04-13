<template>
    <div class="links-menu footer">
        <div class="logo pointer">
            <img src="../assets/avada-music-logo.png" alt="Logo">
        </div>
        <ul>
            <li v-for="(link, index) in links" class="pointer" :class="index==0?'active':''">{{links[index]}}</li>
        </ul>
    </div>
    <div class="footer-social links-menu">
        <p>@ copyright 2012 - 2020 1 AVADATHEMEBYTHEMEFUSION | ALL RIGHTSRESERVED | POWERED BY WORDPRESS</p>
        <div class="social">
            <i class="fa-brands fa-square-facebook pointer"></i>
            <i class="fa-brands fa-square-twitter pointer"></i>
            <i class="fa-brands fa-square-instagram pointer"></i>
            <i class="fa-brands fa-square-youtube pointer"></i>
        </div>
    </div>
</template>

<script>

    export default {
        name: 'Footer',
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


<style lang="scss">

    .footer {
        background-color: #323844;
        & ul {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 15px;
            font-size: 12px;
            color: #6a6e78;
        }
    }

    .footer-social {
        background-color: #252a33;
        & p {
            font-size: 7px;
            color: #6a6e78;
        }
        & .social {
            color: #323844;
            font-size: 15px;
            & i {
                padding: 5px;
            }
        }
    }

</style>