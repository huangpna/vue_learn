<template>
  <div id="app">
    <child v-bind:message="parentMsg" v-on:listenToChildEvent="showMsgFromChild"></child>
    <componentsA></componentsA>
    <componentsB></componentsB>
  </div>
</template>

<script>
  import child from './components/Child.vue'
  import componentsA from './components/componentsA.vue'
  import componentsB from './components/componentsB.vue'
export default {
  name: 'App',
  data(){
    return{
      parentMsg:"hello,hello"
    }
  },
  methods:{
    showMsgFromChild:function (data) {
      console.log(data);
    }
  },
  components:{
    child,
    componentsA,
    componentsB
  }
}
</script>
