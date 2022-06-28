<template>
   <div>
  
  </div>
</template>

<script>
 let arr = [{a:100}, {a: 20}, {a:-10}]
    const sum = arr.reduce((pre,curr) => {
  return pre+curr.a
},0)
console.log(sum)

let stess = 'abaaacdadbcadcbadcb'
let str = stess.split('')
// console.log(str);
let add = str.reduce((allNum,curr) => {
  if(curr in allNum) {
    allNum[curr]++
  }else{
    allNum[curr] =1
  }
  return allNum
},{})
console.log(add);


// http://www.baidu.com?name=zhangsan&age=18&sex=nan#
// 解析出
// {name: 'zhangsan',age: 18, sex: 'nan' }
let url = 'http://www.baidu.com?name=zhangsan&age=18&sex=nan#'
const process = (url)=>{
  const index1 = url.indexOf('?'),
        index2 = url.indexOf('#'),
        params = url.slice(index1+1,index2 ).split('&')
  return params.reduce((pre,curr)=>{
    const [key,value] = curr.split('=')
    pre[key] = value
    return pre
  },{})
}

console.log(process(url));




export default {
  name: 'App',
  data() {
   return{
     
   }
    
  },
  methods:{
   
  }
}
</script>

<style >
 

</style>
