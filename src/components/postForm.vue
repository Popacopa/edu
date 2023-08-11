<template>
        <form action="" @submit.prevent>
            <input v-model="post.title" type="text" placeholder="название">
            <input v-model="post.body" type="text" placeholder="описание">
            <button class="enter" @click="createPost">enter</button>
        </form>
</template>

<script>
    export default {
        data() {
            return {
                post: {
                    title: '',
                    body: '',
                }
            }
        },
        methods: {
            createPost() {
                this.post.id = Date.now()
                this.$emit('create', this.post)
                this.post = {title: '', body: ''}
            }
        }
    }
</script>

<style lang="scss" scoped>
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
    .enter {
        width: 100px;
        height: 60px;
        border-radius: 20px;
        border: none;
        background-color: rgba(255, 255, 255, 0.398);
        font-family: 'Montserrat', sans-serif;
        font-size: large;
        transition: all 0.2s;
        cursor: pointer;
        &:hover {
            box-shadow: 1px -1px 25px 0px rgba(64, 83, 97, 0.14);
            transform: scale(0.9, 0.9);
        }
    }
</style>