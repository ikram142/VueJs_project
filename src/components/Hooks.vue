<template>

 <h1>{{property}}</h1>

  </template>

<script>

export default {
 beforeCreate() {
    alert('Nothing gets called before me!')
  },
  data() {
    return {
      property: 'Blank'
    }
  },

  computed: {
    propertyComputed() {
      alert('I change when this.property changes.')
      return this.property
    }
  },

  created() {
    this.property = 'Example property update.'
    alert('propertyComputed will update, as this.property is now reactive.')
  }
,
beforeMount() {
    alert(`this.$el doesn't exist yet, but it will soon!`)
  },
  Mount() {
    alert(`mounted!`)
  },
  beforeUpdate(){
        alert(`tbefore update`)

  },
  Update(){
        alert(`updated!`)

  }

}
</script>
<style>

</style>
