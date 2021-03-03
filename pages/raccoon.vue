<template>
    <div class="raccoon">
        <header/>
    <div class="content">
        <h2 class="title"> Raccoon Internet</h2>
        <sidebar class="sidebar"/>
        <div class="child">
            <NuxtChild />
        </div>
    </div>
      
    </div> 
</template>
<script>
export default {
    layout:'header'
}
</script>
    
<style scoped>
    /* .raccoon{
        background-color: darkorange !important;
    } */
</style>