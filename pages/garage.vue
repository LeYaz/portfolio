<template>
    <div>
        <header/>
    <div class="content">
        <h2 class="title"> Garage </h2>
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
    
</style>