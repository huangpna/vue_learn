<template>
  <div>
      <div>{{btext}}</div>
  </div>
</template>
<script>
  import bus from '../assets/eventBus'
  export default {
    name:'componentsB',
    data () {
      return {
        'btext':"我是B组件内容"
      }
    },
    created:function(){
      this.bbtn();
    },
    methods:{
      bbtn:function(){
        bus.$on("myFun",(message)=>{   //这里最好用箭头函数，不然this指向有问题
          this.btext = message
        })
      }
    }
  }
</script>
