<template>
  <div id="languages">
    <ul>
    <li v-for="lg in languages"   :key="lg.id" >
     <h3>{{lg.text}}</h3> 
     <p >{{lg.degree}} </p>
      </li></ul></div>
  </template>

<script>

export default {
  props:['languages'],
  data(){
    return {
      languages:Array,
      required:true
       
           }
  }
}
</script>