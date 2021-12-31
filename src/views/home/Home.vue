<template>
  <div id="home">
    <nav-bar class='home-nav'>
      <div slot="center">购物街</div>
    </nav-bar>
    
  </div>
</template>
<script>
import NavBar from '@/components/common/navbar/NavBar';
import {getHomeMultidata} from 'network/home';
export default {
name: 'Home',
  data() {
    return {
      result: null
  }
},
  methods: {
},
  components: {
    NavBar
    
  },
  created() {
    getHomeMultidata().then(res=>{
      // console.log(res)
      this.result = res;
    })
  },
  mounted() {
  }
}
</script>
<style scoped>
.home-nav {
  background-color: var(--color-tint);
  color: var(--color-background);
}

</style>