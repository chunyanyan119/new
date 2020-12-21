<template>
  <div class="tab-bar-item" @click="itemclick">
    <div v-if="!IsActive"><slot name="item-icon"></slot></div>
    <div v-else> <slot name="active-item-icon"></slot></div>
<!--    下面的是给定颜色-->
<!--   <div :class="{active:IsActive}"><slot name="item-text"></slot></div>-->
<!--    下面的是 可以动态变颜色 -->
    <div :style="activeStyle"><slot name="item-text"></slot></div>
  </div>
</template>

<script>
export default {
name: "TabBarItem",
  props:{
  path: String,
  activeColor:{
    type: String,
    default: 'red'
  }
  },
  data(){
  return {
    // path:'/home'

  }
  },

  computed:{
    IsActive(){
      return this.$route.path.indexOf(this.path) !==-1
    },
    activeStyle(){
      return this.IsActive ? {color:this.activeColor} : {}
    }

  },
  methods:{
    itemclick(){
      this.$router.replace(this.path)
    }
  }
}

</script>

<style scoped>
.tab-bar-item{
  flex:1px;
  text-align: center;
  height: 49px;
  margin-bottom: 5px;
  font-size: 14px;

}

.tab-bar-item img{
  width: 24px;
  height: 24px;
  margin-top: 3px;
  vertical-align: middle;
  margin-bottom: 2px;
}
/*.active{*/
/*  color:red;*/
/*}*/

</style>

