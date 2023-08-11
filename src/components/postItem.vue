<template>
    <div class="post">
        <div class="main">
            <div class="title"><strong>{{ post.title }}</strong></div>
            <div class="body">{{ post.body }}</div>
        </div>
        <div>
            <main-button class="delete">delete</main-button>
        </div>
    </div>
</template>

<script>
import mainButton from './UI/main-button.vue'
    export default {
  components: { mainButton },
        props: {
            post: {
                type: Object,
                required: true,
            }
        }
    }
</script>

<style lang="scss" scoped>
    .post {
        border-radius: 20px;
        padding-left: 20px;
        padding-right: 20px;
        height: 10vh;
        display: flex;
        //flex-direction: column;
        align-items: center;
        justify-content: space-between;
        margin-top: 14px;
        font-family: 'Montserrat', sans-serif;
        background-color: rgba(255, 255, 255, 0.398);
        transition: all 0.5s;
        .title {
            font-size: large;
        }
        &:hover {
            //box-shadow: 1px -1px 25px 0px rgba(64, 83, 97, 0.14);
            transform: scale(1.1, 1.1);
        }
    }
    .delete {
        transform: scale(0.9, 0.9);
        &:hover {
            background-color: rgba(255, 93, 93, 0.75);
            box-shadow: 1px -1px 25px 0px rgba(64, 83, 97, 0.14);
            transform: scale(0.8, 0.8);
        }
    }
</style>