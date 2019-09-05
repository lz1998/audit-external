<template>
  <div class="home">
    <router-view></router-view>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import {test} from '@/api/test.js'

export default {
  name: 'home',
  components: {
  },
  mounted() {
    test().then(res=>{
      console.log(res)
    })
  }
}
</script>
