<template>
  <div>
    <a @click="one" href="http://www.baidu.com">阻止百度</a>
    <br>
    <a @click="two(10, $event)" href="http://www.baidu.com">阻止去百度</a>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return{
     
    }
  },
  methods:{
    one(e){
      e.preventDefault();

    },
    two(num, e){
      e.preventDefault();
      console.log(num);
      console.log(e);
    }
  }
}
</script>

<style>

</style>
