<template>

    <div class="blog-container">
        <div v-for="(post, index) in posts" :class="blogClass + index" class="post pointer" :style="{'backgroundImage': `url(${post.img})`}"
        @mouseover="showTitle=index" @mouseleave="showTitle=null">
           <div class="on-hover" v-show="showTitle==index">
            <h1>{{post.title}}</h1>
           </div>
            <div class="post-text">
                <h4>{{ post.title }}</h4>
                <p>{{ post.subtitle }}</p>
            </div>

        </div>
    </div>

    <img src="" alt="">
</template>

<script>
    export default {
        name: 'Post',
        data() {
            return {
                posts: [
                    {
                        img: '/src/assets/blog_flavor_rock-400x200.jpg',
                        title: 'The flavor of rock',
                        subtitle: 'Sed sit amet turpis. Curabitur cursus lacinia est at interdum risus id condimentum'
                    },
                    {
                        img: '/src/assets/blog_music_techo-400x200.jpg',
                        title: 'Technology and music',
                        subtitle: 'Sed sit amet turpis. Curabitur cursus lacinia est at interdum risus id condimentum'
                    },{
                        img: '/src/assets/blog-post3-200x300.jpg',
                        title: 'While my guitar weeps',
                        subtitle: 'Sed sit amet turpis. Curabitur cursus lacinia est at interdum risus id condimentum'
                    },{
                        img: '/src/assets/blog-post4-200x300.jpg',
                        title: 'It just sounds better',
                        subtitle: 'Sed sit amet turpis. Curabitur cursus lacinia est at interdum risus id condimentum'
                    },{
                        img: '/src/assets/blog-post1-200x300.jpg',
                        title: 'Taking it back to the old school',
                        subtitle: 'Sed sit amet turpis. Curabitur cursus lacinia est at interdum risus id condimentum'
                    },{
                        img: '/src/assets/blog-post2-200x300.jpg',
                        title: 'Sharing the stage with a legend',
                        subtitle: 'Sed sit amet turpis. Curabitur cursus lacinia est at interdum risus id condimentum'
                    },
                ],
                blogClass: 'blog',
                showTitle: null
            }
        },
        methods: {
        }
    }
</script>

<style lang="scss">
@use '../styles/variables' as *;

    .on-hover {
        background-color: $red;
        color: white;
        text-align: center;
        width: 100%;
        height: 100%;
        opacity: 0.7;
    }
    .blog-container {
        display: grid;
        grid-template-columns: repeat(6, 1fr);
        grid-template-rows: repeat(8, 1fr);
        grid-column-gap: 12px;
        grid-row-gap: 12px;
        height: 800px;
        width: 1000px;
        margin: auto;
        padding: 40px;
          
    }

    .post {
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
        position: relative;
        & img {
            width: 100%;
            height: calc(100% - 70px)
        } 
    }

    .post-text {
        background-color: #323844;
        text-align: left;
        padding: 15px;
        margin: 0;
        position: absolute;
        left: 0;
        bottom: 0;
        width: 100%;
        & h4 {
            color: $red;
        }
        & p {
            color: #828092;
            margin: 0;
            font-size: 10px;
            width: 100%;
            padding-top: 5px;
        }
    }

    .blog1 { grid-area: 1 / 1 / 3 / 5; }
    .blog2 { grid-area: 3 / 1 / 7 / 3; }
    .blog3 { grid-area: 3 / 3 / 7 / 5; }
    .blog4 { grid-area: 1 / 5 / 5 / 7; }
    .blog5 { grid-area: 5 / 5 / 9 / 7; }
    .blog0 { grid-area: 7 / 1 / 9 / 5; }

</style>