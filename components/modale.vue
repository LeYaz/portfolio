<template>
  <div class="bloc-modale" v-if="revele">
    <div class="overlay" v-on:click="toggleModale"></div>

    <div class="modale">
      <div v-on:click="toggleModale" class="btn-modale btn btn-danger">X</div>
      <h2>{{cards[index].name}}</h2>
      <div class="img-container">
        <div class="btn-change" v-on:click="previous">⪡</div>
        <img class="img-modale" v-bind:src="cards[index].src">
        <div class="btn-change" v-on:click="next">⪢</div>
      </div>
      
      
    </div>
  </div>
</template>


<script>
export default {
  name: "Modale",
  props: ["revele", "toggleModale", "cards", "index"],
  methods : {
    next: function(){
      if(this.index<this.cards.length-1){
        console.log(this.index)
        this.index++
      }else{
        this.index=0;
      }
    },
    previous: function(){
      if(this.index!=0){
        this.index--
      }else{
        this.index=this.cards.length-1;
      }
    }
  }
};
</script>


<style scoped>
.bloc-modale {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}

.overlay {
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
}

.modale {
  background: #f1f1f1;
  color: #333;
  padding: 50px;
  position: absolute;
  top: 10%;
}

.modale h2{
  text-align: center;
}

.btn-modale {
  position: absolute;
  top: 10px;
  right: 10px;
  cursor: pointer;
}

.btn-modale:hover{
  color: red;
}

.img-modale{
  width:600px;
  height: auto;
  margin: auto;
}

.btn-change{
  font-size: 60px;
  cursor: pointer;
  margin-left: 20px;
  margin-right: 20px;
}

.img-container{
  display: flex;
  flex-direction: row;
  align-items: center;
}

.btn-change:hover{
  color: red;
  transform: scale(1.2);
}
</style>