<template>
  <div class="container">
    <div class="home" id="header">
        <div class="logo-home">
           <nuxt-link to="/" id="home-link"> <img src="~/assets/img/logo.svg"></nuxt-link>
        </div>
        <div class="div-sub-title-home">
            <h3 class="sub-title-home">Developpeur fullstack</h3>
        </div>
        <div class="project-link">
            <ul>
                <li><nuxt-link id="link-raccoon" to="/raccoon">Raccoon Internet</nuxt-link></li>
                <li><nuxt-link id="link-tetris" to="/tetris">Tetris</nuxt-link></li>
                <li><nuxt-link id="link-quizz" to="/quizz">Quizz champions</nuxt-link></li>
                <li><nuxt-link id="link-garage" to="/garage">Garage app</nuxt-link></li>              
            </ul>
        </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
html, body{
    margin: 0;
    padding: 0;
    overflow-x: hidden;
    color: white;
    height: 100%;
}

body{
    background-color: white;
}
.home{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 100%;
    height: 100vh;
    background-color: black;
}





.logo-home{
    width: 300px;
    margin: auto;
    margin-top: 50px;
    animation: slideInFromLeft 2s linear;
}

.logo-home img{
    width: 300px;
    height: 300px;
    animation: rotate 1s linear 2;
}

.sub-title-home{
    opacity: 0;
    animation: slideInFromRight 2s linear 2s forwards;
    color: white;
    text-transform: uppercase;  
    text-align: center;
}

.project-link{
    margin-top: 200px;
}

.project-link ul {
    display: flex;
    flex-direction: row;
    padding-inline-start: 0px;
    
}
.project-link ul li{
    list-style: none;
    flex: 1;
    text-align: center;
    margin: auto;
    transition: 0.5s;
    
}

.project-link ul li a{
   text-decoration: none;
   text-transform: uppercase;
   color: white;
   transition: 0.5s;
   animation: fonduEffect 3s linear 4s forwards;
    opacity: 0;
}

.project-link ul li:hover{
    transform: scale(1.2);
    
    
 }

 .project-link ul li a:hover{
    color: grey !important;
    
 }


 /*   KEYFRAMES   */
@keyframes slideInFromLeft{
    0%{
        transform: translateX(-300%);      
    }
    100%{
        transform: translateX(0%);   
    }
}

@keyframes slideInFromRight{
    0%{
        transform: translateX(100%);
        opacity: 0;
    }
    100%{
        transform: translateX(0%);
        opacity: 1;
    }
}

@keyframes fonduEffect{
    0%{  
        opacity: 0;
    }
    100%{ 
        opacity: 1;
    }
}

@keyframes rotate{
    0%{
        transform: rotate(-360deg);
    }
    100%{
        transform: rotate(0deg);
    }
}

@keyframes headerAnimation{
    0%{
        height: 100%;
        border-bottom-left-radius: 10%;
        border-bottom-right-radius: 50%;
    }

    50%{
        height: 150px;
        border-bottom-left-radius: 20%;
        border-bottom-right-radius: 20%;
        transform:translateX(-50px);
    }
    65%{
        
        border-top-right-radius: 50%;
        border-bottom-right-radius: 50%;
    }
    100%{
        

    }
}



@keyframes headerLogoAnimation{
    0%{
        height: 150px;
        width: 150px;
    }

    100%{
        height: 100px;
        width: 100px;
    }
}
</style>
