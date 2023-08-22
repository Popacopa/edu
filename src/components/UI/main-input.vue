<template>
  <input :value="value" @input='updateInput' name="" id="">
</template>

<script>
  export default {
    name: 'main-input',
    props: {
      value: [String, Number],
    },
  methods: {
    updateInput(event) {
      this.$emit('update:value', event.target.value)
    }
  },
  }
</script>

<style lang="scss" scoped>
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
</style>