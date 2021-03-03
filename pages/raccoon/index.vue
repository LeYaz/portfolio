<template>
    <div class="presentation">
        <h3>Le projet</h3>
        <p> Raccoon Internet est un site web vitrine développé pour l'entreprise du même nom.</p>
        <p>Sur ce site je me suis occupé du développement from scratch, et de la mise en ligne.</p>
        <h3>Aperçu</h3>
        
        
        <div class="img-container">
            <modale :revele="revele" :toggleModale="toggleModale" :cards="cards" :index="index"/>
            <div v-for="(card, index) in cards" :key="card.name" v-on:click="openModale(index)" class="card" v-bind:class="{'card-anim':!anim }">
                <img class="raccoon-img" v-bind:src="card.src">
                <h6>{{card.name}}</h6>
            </div>
        </div>
        
    </div> 
</template>
<script>
import modale from '../../components/modale.vue';
export default {
  components: { modale },
    data(){
        return{
            cards: [
                {
                    name: 'Accueil',
                    src: require('/assets/img/raccoon/raccoon.PNG')
                },
                {
                    name: 'Qui sommes nous',
                    src: require('~/assets/img/raccoon/equipe.PNG')
                },
                {
                    name: 'Contact',
                    src: require('~/assets/img/raccoon/contact.png')
                },
                {
                    name: 'Devis',
                    src: require('~/assets/img/raccoon/devis.PNG')
                },
                {
                    name: 'Service',
                    src: require('~/assets/img/raccoon/service.PNG')
                },
                {
                    name: 'Réalisations',
                    src: require('~/assets/img/raccoon/realisations.png')
                },
                {
                    name: 'Menu',
                    src: require('~/assets/img/raccoon/menu.PNG')
                }
            ],
            revele:false,
            index: 0,
            anim: false
        }
    
    },
    methods :{
        toggleModale: function(){
            this.revele = !this.revele;     
            this.anim = true;           
        },
        openModale: function(index){
            this.anim = true;
            this.revele = !this.revele;           
            this.index = index;
            // let cardsanim = document.querySelectorAll(".card-anim");
            // console.log(cardsanim)
            // cardsanim.forEach(element => {
            //     element.classlist.remove("card-anim");
            // });
            
        }

    },
    pageTransition: {
        name: 'page',
        mode: 'out-in',
        beforeEnter (el) {
        console.log('Before enter...');
        }
    }
}
</script>
    
<style scoped>
    .presentation{
        display: flex;
        flex-direction: column;
    }

    h3{
        flex:1;
        text-align: center;
    }
    
    p{
        flex: 1;
        text-align: justify;
        width: 60%;
        margin: auto;
    }

    .video-container{
        flex: 1; 
        width: 320px;
        margin: auto;
    }

    .video-container video{
        margin: auto;

    }
    .img-container{
        display: flex;
        width: 100%;
        height: 100%;
        flex-wrap: wrap;
        align-items: center;
        margin-top: 10px;
    }
    .raccoon-img{
        
        width: 100%;
        height:100%;
        margin: auto;
       
        transition: 1s;
    }
    .card{
        width: 300px;
        height: auto;
        margin: auto;
        border: 1px solid black;
        background-color: black;
        /* margin-top: 10px; */
        /* align-self: center; */
        
        
    }

 
    

    .card h6{
        text-align: center;
        /* background-color: black; */
        color: blanchedalmond;
        margin: 10px;
    }

    .card:hover{
        transform: scale(1.1);
        cursor: pointer;
        /* background-color: grey; */
        opacity: 0.8;
    }

    /* .card:hover h6{
        color: black;
        
    }

    .card:hover img{
        
        border-bottom: 1px solid black;
    } */
    
    .card-anim:nth-child(odd){
        
        animation: slideInFromLeft 3s  ease-in-out;
        /* animation-delay: 2s; */
        /* opacity: 0; */
    }

    .card-anim:nth-child(even){
        animation: slideInFromRight 3s ease-in-out;
        /* animation-delay: 2s; */
        /* opacity: 0; */
    }

    @keyframes slideInFromLeft{
        0%{
            transform: translateX(-300%);   
            opacity: 1;   
        }
        100%{
            transform: translateX(0%);  
            opacity: 1; 
        }
    }

    @keyframes slideInFromRight{
        0%{
            transform: translateX(300%);
            opacity: 1;
            
        }
        100%{
            transform: translateX(0%);
            opacity: 1;
        }
    }

</style>