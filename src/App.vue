<template>

  <h3>我是App组件</h3>
</template>

<script>

import {reactive,isProxy, readonly, toRefs,ref,isRef,isReactive,isReadonly} from "vue";
export default {
  name:'App',
  setup(){
    let car = reactive({
      name:'奔驰',
      price:'40W'
    })
    let sum = ref(0)
    let car2 = readonly(car)

    console.log(isRef(sum))
    console.log(isReactive(car))
    console.log(isReadonly(car2))
    console.log(isProxy(car))
    console.log(isProxy(car2))

    return{...toRefs(car)}
  }
}
</script>

<style scoped>
.app {
  background-color: gray;
  padding: 10px;
}
</style>