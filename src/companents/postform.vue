<template>
    <form @submit.prevent>
        <input v-model="post.title" type="text" @input="title = $event.target.value" placeholder="Post Title">
        <input v-model="post.post" type="text" @input="post = $event.target.value" placeholder="Post...">
        <button @click="createPost">Post</button>
    </form>
</template>

<script>
export default {
    data() {
        return {
            post: {
                title: "",
                post: ""
            }          
        }
    },
    methods: {
        createPost() {
            tjis.post.id = Date.now()
            this.$emit("create", this.post)
            this.post = {
                title: "",
                post: ""
            }
        }
    }
}
</script>

<style>
    
</style>