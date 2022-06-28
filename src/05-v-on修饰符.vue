<template>
  <div @click="fatherFn">
    <button @click.stop="btn">阻止事件冒泡</button>
    <br>
    <a href="http://www.baidu.com" @click.prevent="btn">阻止默认行为</a>
    <br>
    <button @click.once="btn">程序运行期间, 只触发一次事件处理函数</button>
    <br>
    <input type="text" @keydown.enter="enterFn">
    <hr>
    <input type="text" @keydown.esc="escFn">
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
   fatherFn(){
     console.log('触发了');
   },
   btn(){
     console.log(666);
   },
   enterFn(){
     console.log('回车键');
   },
   escFn(){
     console.log('esc键');
   }
  }
}
</script>

<style>

</style>
