<template>
    <div class="post">
        <div class="main">
            <div class="title"><strong>{{ post.title }}</strong></div>
            <div class="body">{{ post.body }}</div>
        </div>
        <div class="delete">
            <button>delete</button>
        </div>
    </div>
</template>

<script>
    export default {
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
            box-shadow: 1px -1px 25px 0px rgba(64, 83, 97, 0.14);
            transform: scale(1.1, 1.1);
        }
    }
    .delete {
        button {
            background-color: rgba(249, 78, 78, 0.85);
            width: 70px;
            height: 40px;
            border: none;
            border-radius: 14px;
            color: white;
            font-family: 'Montserrat', sans-serif;
            box-shadow: 1px -1px 25px 0px rgba(64, 83, 97, 0.14);
            cursor: pointer;
        }
    }
</style>