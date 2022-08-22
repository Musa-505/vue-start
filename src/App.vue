<template>
    <div class="App">
        <postform @create="createPost"/>
        <postlist :posts="posts"/>
    </div>
</template>

<script>
import postform from './companents/postform.vue';
import postlist from './companents/postlist.vue';
export default {
    components: [
        postlist,
        postform
    ],
    data() {
        return {
            posts: [
                { id: 1, title: "Post", body: "Hollo wtf this is new post" },
                { id: 2, title: "Post", body: "Hollo wtf this is new post" },
                { id: 3, title: "Post", body: "Hollo wtf this is new post" },
            ]
        };
    },
    methods: {
        createPost(post) {
            this.posts.push(post);
        }
    },
    components: { postform, postlist }
}
</script>

<style>
    .ios{
        font-family: sans-serif;
        border-radius: 10px;
        border: 2px solid teal;
        margin: 15px;
        padding: 5px;
    }
</style>