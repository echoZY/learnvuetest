<template>
  <div class="tabbar">
    <slot>
    </slot>
  </div>
</template>
<script>
export default {
name: 'Tabbar',
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
.tabbar{
  display: flex;
  justify-content: space-around;
  align-items: center;
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  height: 46px;
  font-size: 14px;
}
</style>