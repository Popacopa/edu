<template>
    <div class="wrapper">
        <postForm @create="createPost"/>
        <postList @remove="removePost" :posts="posts"/>
    </div>
</template>

<script>
    import postForm from '@/components/postForm.vue'
    import postList from '@/components/postList.vue'
    export default {
        components: {
            postForm, postList
        },
        data() {
            return {
                posts: [],
            }
        },
        methods: {
            createPost(post) {
                this.posts.push(post)
            },
            removePost(post) {
              this.posts = this.posts.filter(p => p.id !== post.id)
            }
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
    .wrapper {
        width: 50vw;
        margin: auto;
    }
    body{
        margin-top: 20px;
        background: linear-gradient(310deg, rgba(0,236,255,1) 0%, rgba(255,226,0,1) 100%);
        //border: 1px solid black;
        min-height: 100vh;
    }
</style>
