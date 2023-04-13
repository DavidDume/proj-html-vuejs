<template>
    <div class="title">
        <div class="topbar"></div>
        <h1>Music Is Life</h1>
        <div class="bottom-bar"></div>
        <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione similique sit quam, eum placeat maxime. Nihil corporis </p>
    </div>

</template>

<script>
    export default {
        name: 'Main'
    }
</script>

<style lang="scss">
    @use '../styles/variables' as *;
    
    .title {
        text-align: center;
        margin: auto;
        width: 600px;
        & .topbar {
            background-color: $red;
            height: 7px;
            width: 40%;
            margin: auto;
        }
        & h1 {
            color: white;
            padding: 20px 0 10px 0;
            letter-spacing: 1px;
            font-size: 30px;
        }
        & .bottom-bar {
            width: 30%;
            height: 1px;
            margin: 0 auto 25px auto;
            background-color: #444e62;
        }
        & p {
            color: white;
            font-size: 12px;
            padding-bottom: 40px;
            width: 70%;
            margin: auto;
            color: #838092;
        }
    }


</style>