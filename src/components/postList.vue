<template>
    <div class="" v-if="posts.length > 0">
        <h4>Список пользователей</h4>
        <postItem @remove="$emit('remove', post)" :post="post" v-for="post in posts" :key="post.id"/>
    </div>
    <p v-else>it is so busy now</p>
</template>

<script>
import postItem from '@/components/postItem.vue'
    export default {
        components: {
            postItem
        },
        props: {
            posts: {
                type: Array,
            }
        }
    }
</script>

<style lang="scss" scoped>
    h4, p  {
       font-family: 'Montserrat', sans-serif;
    }
</style>