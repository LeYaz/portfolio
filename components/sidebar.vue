<template>
  <div>
      <ul class="list-sidebar">
          <li><NuxtLink class="link" v-bind:to="baseUrlPresentation">Présentation</NuxtLink></li>
          <li><NuxtLink class="link" v-bind:to="baseUrlTechnologie">Technologies</NuxtLink></li>
          <li><NuxtLink class="link" v-bind:to="baseUrlLiens">Liens</NuxtLink></li>
          <!-- <li><a></a></li> -->
      </ul>
  </div>    
</template>
<script>
export default {
    data(){
        return{
            baseUrlPresentation: this.$route.matched[0].path+'/',
            baseUrlTechnologie : this.$route.matched[0].path+'/technologies',
            baseUrlLiens: this.$route.matched[0].path+'/liens'
        }
    }
    
}

</script>
<style scoped>

ul{
    padding: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 100%;
    width: 100%;
    margin-block-start: 0px;
    margin-block-end: 0px;
    transform: translateX(50%);
    
}
ul li {
    flex: 1;
    list-style: none;
    height: 30%;
    width: 100%;
    margin: auto;  
    display: flex;
    
    
}

.link{
    text-decoration: none;
    text-transform: uppercase;
    height: 100%;
    width: 70%;
    margin: auto;
    color: grey !important;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: grey;
    /* border-radius:20%; */
    border-top-left-radius:50% ;
    border-bottom-left-radius:50% ;
    transition: 1s;
    
}


 .nuxt-link-exact-active{
    background-color: black !important;
    color: white !important;
    transform: translateX(-30%);
    
}

.link:hover{
    transform: translateX(-50%);
    background-color: black;
    
}
</style>