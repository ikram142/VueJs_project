<template>
<footer>
 <h1>{{copyrigth}}:{{title}}</h1>
</footer>
  </template>

<script>
import {bus} from '../main'
export default {

  props:
  {title:{
    type:String
  }},
  data(){
    return {
      copyrigth:"copyrigth 2018"
           }
  },
  created(){
 bus.$on('titleChanged',(data)=>{
   this.title=data
 })
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
