<template>
  <div>
   <h1>{{ message }}</h1>
   <button @click="btn">逆转世界</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return{
     message: 'Hello world'
    }
  },
  methods:{
    btn(){
      this.message = this.message.split('').reverse().join('')
    }
  }
}
</script>

<style>

</style>
