<template>
  <div id="app">
    <!-- <UserInfo :title="myTitle" @changeTitle = 'handleChange'></UserInfo> -->
    <!-- <UserName
      :username="username"
      :age="age"
      :isSingle="isSingle"
      :car="car"
      :hobby="hobby"
    ></UserName> -->
    <BaseProgress
      :w="width"
      >
    </BaseProgress>
    <BaseCount :count="count" @changeCount = "handleChange"></BaseCount>
    <HmWorld></HmWorld>
  </div>
</template>

<script>
//通过props传递数据
// 1、在组件中通过props选项，声明需要接收的外部数据(例如:count="count")
// 2、在父组件中，使用子组件的时候，通过v-bind动态绑定数据(例如:count="count")
// 3、在子组件中，使用props选项,配置props选项，设置需要接收的外部数据的名称和类型(props:['count'])
// 4、在子组件中，通过props定义的属性，直接在模板中使用(例如:插值表达式{{count}})
// 5、在子组件中，通过props接收到的外部数据，是只读的，不能修改。如果修改需要先请求父组件修改

//通过$emit请求修改父组件的数据
// 1、在子组件中，通过$emit()触发自定义事件，通知父组件修改数据
// 2、在子组件中,通过$emit()设置一个自定义处理函数,用于处理修改数据的逻辑
// 3、然后返回父组件中，找到子组件的标签,输入自定义的事件处理函数
// import UserInfo from './components/UserInfo.vue';
// import UserName from './components/UserName.vue';
import BaseProgress from './components/BaseProgress.vue'
import BaseCount from './components/BaseCount.vue';
import HmWorld from './components/HmWorld.vue';
export default {
  components: {
    // UserInfo,
    // UserName,
    BaseProgress,
    BaseCount,
    HmWorld
  },
  data() {
    return {
      myTitle: '黑马程序员',
      username: '小帅',
      age: 28,
      isSingle: true,
      car: {
        brand:'宝马',
      },
      hobby: ['篮球', '足球', '羽毛球'],
      width: 20,
      count:100
    }
  },
  methods: {
    handleChange(value) {
      this.count = value
    }
  }
}
</script>


