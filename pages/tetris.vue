<template>
    <div>
        <!-- <header/> -->
    <div class="content">
        <h2 class="title"> Tetris </h2>
        <sidebar class="sidebar"/>
        <div class="child">
            <NuxtChild />
        </div>
    </div>
    
        
    </div> 
</template>
<script>
export default {
    layout:'header',
    // fetch({redirect}){
    //     redirect('/presentation')
    // }
}
</script>
    
<style scoped>
    
</style>