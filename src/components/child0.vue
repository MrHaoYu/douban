<template lang="html">
  <div class="">
    {{message}}+{{size}}
    <button type="button" name="button" @click="toValue">传值给父亲</button>
    <button type="button" name="button" @click="send">传值给兄弟</button>
  </div>

</template>

<script>
import vm from "./vm.js"
export default {
  name: 'child0',
  props:['message','size'],
  data(){
    return {
      a:'我是child0的数据'
    }
  },
  methods:{
    toValue(){
      this.$emit('ee','儿子' )
    },
    send(){
      vm.$emit('child0-msg',this.a)
    }
  }
}
</script>

<style lang="css">

</style>
