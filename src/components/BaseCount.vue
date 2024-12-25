<template>
  <div class="base-count">
    <button @click="sub()">-</button>
    <span>{{ count }}</span>
    <button @click="add()">+</button>
    <HmWorld></HmWorld>
  </div>
</template>

<script>
export default {
    props: {
      count:Number
    },
  methods: {
    sub() {
      this.$emit('changeCount',this.count-1)
    },
    add() {
      this.$emit('changeCount',this.count+1)
    }
  }
}
</script>

<style>
.base-count {
  margin: 20px;
}
</style>