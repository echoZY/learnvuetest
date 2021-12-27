<template>
  <div class="nav-bar">
    <div class="left">
      <slot name="left">111</slot>
    </div>
    <div class="center">
      <slot name="center">11</slot>
    </div>
    <div class="right">
      <slot name="right">333</slot>
    </div>
  </div>
</template>
<script>
export default {
name: 'NavBar',
  data() {
    return {
  }
},
  methods: {
},
  components: {},
  created() {},
  mounted() {
  }
}
</script>
<style scoped>
.nav-bar{
  display: flex;
  justify-content: space-between;
  align-items: center;
  line-height: 44px;

}
.left,.right{
  background-color: green;
  width: 60px;
}
.center{
  background-color: purple;
  flex: 1;
}
</style>