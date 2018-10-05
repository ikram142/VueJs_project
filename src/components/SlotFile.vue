<template>
<div>
    <div id="form-header">
        <slot name="form-header"></slot>
    </div>
    <div id="form-fields">
        <slot name="form-fields"></slot>
    </div>
    <div id="form-control">
        <slot name="form-control"></slot>
    </div>
    <div id="useful-links">
            <ul >
                <li ><a href="#">link 1</a></li>
                <li ><a href="#">link 2</a></li>
                <li ><a href="#">link 3</a></li>
                <li ><a href="#">link 4</a></li>

            </ul>
        </div>




 
</div>
  </template>

<script>

export default {
 data(){
     return{
         title:'this is a bla bla ba blaaaaaaaaaaaa title'
     }
 }

}
</script>
<style>

</style>
