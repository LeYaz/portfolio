
<template>
    <div>
        <header/>
    <div class="content">
        <h2 class="title"> Quizz </h2>
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
    /* body {
        background-color: darkorchid !important;
    } */
</style>