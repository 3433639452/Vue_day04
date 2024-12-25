<template>
  <div id="app">
    姓名：{{ username }}
    年龄：{{ age }}
    是否单身：{{ isSingle ? '是' : '否' }}
    座驾：{{ car.brand }}
    爱好：{{ hobby.join('、') }}
  </div>
</template>

<script>
export default {
  props:['username','age','isSingle','car','hobby']
}
</script>

<style>

</style>