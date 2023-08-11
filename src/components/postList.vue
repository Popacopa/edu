<template>
    <div class="">
        <h4>Список пользователей</h4>
        <postItem :post="post" v-for="post in posts" :key="post.id"/>
    </div>
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
    h4 {
       font-family: 'Montserrat', sans-serif;
    }
</style>