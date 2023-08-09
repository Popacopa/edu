<template>
    <div class="wrapper">
        <form action="">
            <input type="text" placeholder="название">
            <input type="text" placeholder="описание">
            <button class="enter">enter</button>
        </form>
        <div v-for="post in posts" class="post">
            <div class="title"><strong>{{ post.title }}</strong></div>
            <div class="body">{{ post.body }}</div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                posts: [
                    {id: 1, title: 'заголовок поста', body: 'описание поста'},
                    {id: 2, title: 'заголовок поста', body: 'описание поста'},
                    {id: 3, title: 'заголовок поста', body: 'описание поста'},
                    {id: 4, title: 'заголовок поста', body: 'описание поста'},
                ]
            }
        },
        methods: {

        }
    }
</script>

<style lang="scss">
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100;400&family=Rubik&display=swap');

    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    .post {
        border-radius: 20px;
        padding-left: 20px;
        height: 10vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
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
    .wrapper {
        width: 50vw;
        margin: auto;
    }
    form {
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        input {
            padding-left: 5px;
            width: 100%;
            margin-bottom: 14px;
            height: 40px;
            border: none;
            border-radius: 10px;
            background-color:  rgba(255, 255, 255, 0.398);
            outline: none;
            font-size: 15px;
            transition: all 0.5s;
            &:hover {
            box-shadow: 1px -1px 25px 0px rgba(64, 83, 97, 0.14);
            }
            &:focus {
                box-shadow: 1px -1px 25px 0px rgba(64, 83, 97, 0.14);
                &::placeholder {color: transparent;}
                transform: scale(1.03, 1.03);
            }
        }
    }
    body{
        margin-top: 20px;
        background: linear-gradient(310deg, rgba(0,236,255,1) 0%, rgba(255,226,0,1) 100%);
        //border: 1px solid black;
        min-height: 100vh;
    }
    .enter {
        width: 100px;
        height: 60px;
        border-radius: 20px;
        border: none;
        background-color: rgba(255, 255, 255, 0.398);
        font-family: 'Montserrat', sans-serif;
        font-size: large;
        transition: all 0.2s;
        &:hover {
            box-shadow: 1px -1px 25px 0px rgba(64, 83, 97, 0.14);
            transform: scale(0.9, 0.9);
        }
    }
</style>
