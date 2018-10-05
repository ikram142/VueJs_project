<template>
<header>
 <h2  v-on:click="changeTitle">{{title}}</h2>
  </header>
  </template>

<script>
import {bus} from '../main'
export default {
  props:{
    title:{
        type:String
  }},
  data(){
    return {
      type:String
           }
  },
  methods:{
    changeTitle:function(){
     // this.$emit('changeTitle',"new Title")
     this.title='something title'
     bus.$emit('titleChanged','new Title')
     
    }
  }
}
</script>
<style>
header
{   background: lightpink;
    padding: 10px;}
h2{ color: black;
text-align: center;
} 
</style>
