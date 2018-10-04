<template>
<footer>
 <h1>{{copyrigth}}:{{title}}</h1>
</footer>
  </template>

<script>
export default {
  props:
  {title:{
    type:String
  }},
  data(){
    return {
      copyrigth:"copyrigth 2018"
           }
  }
}
</script>
<style>
footer
{   background: #222;
    padding: 2px;
    position: fixed;
    left: 0;
    bottom: 0;
    width: 100%;
   
    }
h1{ 
    color: lightpink;
    text-align: center;
} 
</style>
