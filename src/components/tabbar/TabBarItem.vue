<template>
  <div class="tab-bar-item" @click="clickItem">
    <slot v-if="!isActive" name="item-icon"></slot>
    <slot v-else name="item-icon-active"></slot>
    <div :style="activeStyle" >
      <slot name="item-content"></slot>
    </div>
  </div>
</template>
<script>
export default {
name: 'TabBarItem',
  data() {
    return {
  }
},
props:{
  path: String,
  defaultColor:{
    type: String,
    default: 'red'
  }
},
methods: {
    clickItem(){
      // console.log(this.path);
      // console.log('router',this.$router);
      this.$router.push(this.path).catch(err=>{
        console.log('输出报错',err);
      })
    }
},
  components: {},
  created() {},
  mounted() {
  },
  computed: {
    isActive(){
      //判断当前选中的
      // console.log('0=========>',this.path);
      // console.log('1=========>',this.$route.path);
      // console.log('2=========>',this.$route.path.indexOf(this.path));
     return this.$route.path.indexOf(this.path) !== -1;
    },
    activeStyle(){
      console.log('222========',this.isActive);
        return this.isActive?{color: this.defaultColor}:{}
    }
  }
}
</script>
<style scoped>
.tab-bar-item{
  text-align: center;
}
.tab-bar-item img{
  vertical-align: middle;
  width: 24px;
  height: 24px;
  margin-top: 3px;
  margin-bottom: 2px;
}
</style>