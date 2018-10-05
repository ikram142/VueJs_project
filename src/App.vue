<template>
  <div >
        <app-header v-bind:title="title" v-on:changeTilte="updatetitle($event)"></app-header>
        <app-firstVue v-bind:languages="languages" ></app-firstVue>
        <app-footer v-bind:title="title"></app-footer>
        <app-hooks></app-hooks>
        <app-slot>
                  <div slot="form-header"><h1>This is the Title</h1>
                                  </div>
                  <h1 slot="form-fields">
                    <input type="text" name="name" placeholder="votre nom" required>
                    <input type="password" name="password" placeholder="votre mot de pass" required>
                  </h1>
                  <h1 slot="form-control">
                    <button type="submit"  v-on:click="handleSubmit">Submit</button>
                  </h1>

        </app-slot>
      </div>    
</template>

<script>
import Hooks from './components/Hooks.vue'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import FirstVue from './components/FirstVue.vue'
import SlotFile from './components/SlotFile.vue'



export default {
  
  components:{

    'app-header':Header,
    'app-footer': Footer,
    'app-firstVue':FirstVue,
    'app-hooks':Hooks,
    'app-slot' :SlotFile

  },
  
  data(){
    return{
      title:'My training',
       languages:[ 
          {id:1,text:'java',degree:'medium1'},
          {id:2,text:'php',degree:'meduim2'},
          {id:3,text:'C++',degree:'meduim3'}]

    }
  },
  methods:{
    updateTitle:function(){
      this.title='updateTitle'
    }
  }
}
</script>

<style>

</style>
