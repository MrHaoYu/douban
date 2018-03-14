<template lang="html">
  <div class="">
      <h3>路由1</h3>
      <p>落叶堆积了好几层
        而我踩过青春听见
      </p>
        <div>
          {{count}}
        </div>
        <child :message="'one'" :size="10" @ee="toParent"></child>
        <child0 :message="'two'" :size="20" @ee="toParent"></child0>
        <child1 />
  </div>

</template>

<script>
import { mapState, mapActions } from 'vuex'
import child from './child'
import child0 from './child0'
import child1 from './child1'

export default {
  name: 'HellowRouter',
  data(){
    return {

    }
  },
  components: {child,child0,child1},
  computed: mapState([
    'count'
  ]),
  methods:{
    toParent(data){
      console.log(data+"传值给父亲")
    }
  }
}
</script>

<style lang="css">
</style>
