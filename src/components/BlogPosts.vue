<template>
    <div class="blog-posts title">
        <h1>Latest Band News</h1>
        <div class="bottom-bar"></div>
        <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione similique sit quam, eum placeat maxime. Nihil corporis 
        </p>
        <div>
            <Post></Post>
        </div>
    </div>
</template>

<script>

    import Post from './Post.vue';

    export default {
        name: 'BlogPosts',
        components: {
            Post
        }
    }

</script>

<style lang="scss">
    .blog-posts {
        width: 80%;
        & p {
            padding-bottom: 0;
        }
    }
</style>