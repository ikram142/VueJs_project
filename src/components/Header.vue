<template>
<header>
 <h2  v-on:click="changeTitle">{{title}}</h2>
  </header>
  </template>

<script>
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
      this.title="new Title"
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
