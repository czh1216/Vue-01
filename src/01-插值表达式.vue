<template>
  <div id="app">
  <h1>{{ msg }}</h1>
  <h2>{{ obj.name }}</h2>
  <h2>{{ obj.ags}}</h2>
  <h3>{{ obj.ags>= 18 ? "成年" : "未成年"}}</h3>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return{
      msg:'Hello World',
      obj: {
        name:'sos',
        ags:17
      }
    }
  }
}
</script>

<style>

</style>
