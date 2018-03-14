<template lang="html">
  <div class="">
    <p>{{a}}</p>
    <p>{{b}}</p>
    接受兄弟间的传值
  </div>
</template>

<script>
import vm from "./vm.js"
export default {
  name: 'child1',
  data () {
     return {
       a: "",
       b: ""
     }
   },
   created: function () {
      vm.$on("child-msg", (e) => {
        this.a = e
      })
      vm.$on("child0-msg",(e) => {
        this.b = e
      })
    },
  methods:{

  }
}
</script>

<style lang="css">

</style>
