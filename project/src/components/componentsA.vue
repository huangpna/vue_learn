<template>
    <div>
      <button @click="abtn">A按钮</button>
    </div>
</template>
<script>
  import bus from '../assets/eventBus'
  export default {
    name:'componentsA',
    data(){
      return{
        msg:'我是组件A'
      }
    },
    methods:{
      abtn:function(){
        bus.$emit("myFun",this.msg)   //$emit这个方法会触发一个事件
      }
    }
  }
</script>
