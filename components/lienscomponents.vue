<template>
  <div class="link">
      <div class="link-projet">
          <h3>Liens des projet</h3>
          <h4><img class="logo" src="~/assets/img/logo/Tetris.png"> Tetris</h4>
            <ul>
                <li><a href="https://github.com/LeYaz/tetris"> Repository Github </a></li>
                <li><a href="https://leyaz.github.io/tetris/"> Site web</a></li>
            </ul>
          <h4> <img class="logo" src="~/assets/img/logo/raccoon.png"> Raccoon Internet </h4>
            <ul>
                <li>Site web plus en ligne</li>
            </ul>  
          <h4> <img class="logo" src="~/assets/img/logo/quizz.png"> Quizz champions </h4>
            <ul>
                <li><a href="https://github.com/LeYaz/game-app">Repository Github </a></li>
            </ul> 
           <h4><img class="logo" src="~/assets/img/logo/car.png"> Garage App</h4>
            <ul>
                <li><a href="https://github.com/LeYaz/FilRouge"> Repository Github </a></li>
            </ul>  
      </div>
      <div class="link-perso">
          <h3>Liens personel</h3>
          <ul>
              <li class="social"> <a href="https://github.com/LeYaz"><img class="logo-social" src="~/assets/img/logo/github.png">  Github</a></li>
              <li class="social"><a href="https://www.linkedin.com/in/yazid-aadnan-webdev/"><img class="logo-social" src="~/assets/img/logo/linkedin.png"> LinkedIn</a> </li>
          </ul>
      </div>
  </div>    
</template>
<script>
export default {
    name: "lienscomponents",
    
}

</script>
<style scoped>
.link{
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.link-projet h3{
   text-align: center;
}

.link-projet h4{
    display: flex;
    align-items: center;
    justify-content: space-evenly;
}

.link-perso li a{
    display: flex;
    align-items: center;
}

.logo{
    width: 40px;
    height: auto;
}

.logo-social{
    width: 40px;
    height: auto;
}

.social span{
    height: 40px;
    vertical-align: middle;
}

.link a {
    text-transform: none;
    text-decoration: none;
    color: black;
}

.link a:hover{
    color: red;
}

.link-perso{
    animation: slideInFromRight 3s  ease-in-out
}

.link-projet{
    animation: slideInFromLeft 3s  ease-in-out
}

@keyframes slideInFromLeft{
        0%{
            transform: translateX(-600%);   
            opacity: 1;   
        }
        100%{
            transform: translateX(0%);  
            opacity: 1; 
        }
    }

    @keyframes slideInFromRight{
        0%{
            transform: translateX(600%);
            opacity: 1;
            
        }
        100%{
            transform: translateX(0%);
            opacity: 1;
        }
    }
</style>