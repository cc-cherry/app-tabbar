<template>
  <div class="tab-bar-item" @click="itemClick">
    <div v-if="!isActive"><slot name="tabbar-icon"></slot></div>
    <div v-else><slot name="tabbar-icon-active"></slot></div>
    <div :style="activeColors"><slot name="tabbar-text"></slot></div>
  </div>
</template>

<script>
    export default {
        name: "TabbarItem",
      data(){
          return{
            // isActive:false
          }
      },
      computed:{
        isActive(){
          return this.$route.path.indexOf(this.path) !== -1
        },
        activeColors(){
          return this.isActive ? {color: this.activeColor} : {}
        }
      },
      props: {
        path: String,
        activeColor:{
          type:String,
          default:"red"
        }
      },
      methods:{
        itemClick(){
          this.$router.replace(this.path)
        }
      }
    }
</script>

<style scoped>
  .tab-bar-item{
    flex: 1;
    text-align: center;
    height: 49px;
    font-size: 14px;
  }
  .tab-bar-item img{
    margin-top: 3px;
    width: 24px;
    height: 24px;
    vertical-align: middle;
    margin-bottom: 2px;
  }
  .active{
    color: red;
  }
</style>
