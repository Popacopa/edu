<template>
    <button class="enter">
        <slot>

        </slot>
    </button>
</template>

<script>
  export default {
        
  }
</script>

<style lang="scss" scoped>
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