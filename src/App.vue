<template>
  <div >
        <app-header v-bind:title="title"></app-header>
        <app-firstVue v-bind:languages="languages" ></app-firstVue>
        <app-footer v-bind:title="title"></app-footer>
      </div>    
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import FirstVue from './components/FirstVue.vue'


export default {
  components:{
    'app-header':Header,
    'app-footer': Footer,
    'app-firstVue':FirstVue

  },
  
  data(){
    return{
      title:'My training',
       languages:[ 
          {id:1,text:'java',degree:'medium1'},
          {id:2,text:'php',degree:'meduim2'},
          {id:3,text:'C++',degree:'meduim3'}]

    }
  }
}
</script>

<style>

</style>
