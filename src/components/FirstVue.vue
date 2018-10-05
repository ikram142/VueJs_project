<template>
  <div id="languages">
   
    <div v-for="(index,lg) in languages"   :key="lg.id" >
     <h3>{{lg.text}}</h3> 
     <p >{{lg.degree}} </p>
      
      <input type="text" name="languages" v-model="lg.value"></div>
      <button v-on:click="addLg">ajouter language</button> 
           <button v-on:click="deleteLg(index)">delete language</button>


      </div>
  </template>

<script>

export default {
  props:['languages'],
  data(){
    return {
     
      Type:Array,
      required:true
       
           }
  },
  methods:{
    deleteLg:function (index) {
      this.languages.splice(index,1)
          },
    addLg:function(){
    
          }

  }
}
</script>