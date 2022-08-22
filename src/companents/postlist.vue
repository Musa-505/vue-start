<template>
    <div class="ios" v-for="post in posts">
        <h1>{{ post.title }}</h1>
        <h3>{{ post.body}}</h3>
    </div>
</template>

<script>
export default {
    props: {
        posts: {
            type: Array,
            required: true
        }
    }
}
</script>

<style>

</style>