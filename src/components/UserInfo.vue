<template>
  <div class="userinfo">
    {{ title }}
    <button @click="changeFn">修改Title</button>
  </div>
</template>

<script>
export default {
  props: ['title'],
  methods: {
    changeFn() {
      this.$emit('changeTitle','传智教育')
    }
  }
}
</script>

<style>

</style>