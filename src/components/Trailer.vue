<template>

    <div class="trailer">
        <p>
            <em>"I just listened to it and said to myself, "Man, I really love this
album." Still, today, it just sounds so fresh. It sounds full of ideas.
These guys knew what they were doing. They're good. And they're
inventive. I haven't heard anything this year that's as inventive. I
don't really expect to."</em></p>
<img src="../assets/band_interview_play_icon.png" alt="" class="pointer">
    </div>

</template>

<script>

    export default {
        name: 'Trailer'
    }

</script>


<style lang="scss">

    .trailer {
        widows: 100%;
        height: 450px;
        background-image: url('../assets/home_slider.jpg');
        background-size: cover;
        background-position: center;
        & p {
            color: white;
            text-align: center;
            padding-top: 150px;
            font-weight: 300;
            letter-spacing: 2px;
            width: 50%;
            margin: auto;
        }
        & img {
            width: 60px;
            margin: 20px auto;
            display: block;
        }
    }

</style>