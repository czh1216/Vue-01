<template>
  <div id="add">
 <p>你要购买商品的数量: {{ count }}</p>
 <button v-on:click="count = count + 1">+1</button>
 <button v-on:click="addFn">+1</button>
 <button v-on:click="addCountFn(5)">+5</button>
 <button @click="subFn">-1</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return{
      count:0
    }
  },
  methods:{
    addFn(){
      this.count++
    },
    addCountFn(val){
      this.count += val
    },
    subFn(){
      this.count--
    }
  }
}
</script>

<style>

</style>
