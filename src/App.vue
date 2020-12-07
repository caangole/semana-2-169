<template>
  <div id="app"> 
    <div class="container-fluid ">
      <div class="row justify-content-center mb-5">
        <div class="col mt-5" v-for="(item, index) of team" :key= "index">
          <TeamCard id="team" v-bind:member="item"></TeamCard>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TeamCard from './components/TeamCard.vue';

export default {
  name: 'App',
  components:{
    TeamCard
  },
  data(){
    return {
      team:[
        {
          codigo: 1,
          nombre: "Carlos González",
          descripcion: "Carlos es un egrasado del programa Mintic 2020 donde perfeccionó sus habilidades como programador senior.",
          rol: "Desarrollador TI",
          imagen: "./pictures/team/carlos.jpg", 
        },
        {
          codigo: 2,
          nombre: "Nicolás Verano",
          descripcion: "Nicolás es un egrasado del programa Mintic 2020 donde perfeccionó sus habilidades como programador senior.",
          rol: "Experto Sistemas IA",
          imagen: "./pictures/team/nicolas.jpg", 
        },
        {
          codigo: 3,
          nombre: "Bugs Bunny",
          descripcion: "Para no olvidar reir Bugs siempre nos acompaña con su ya conocido '¿Que hay de nuevo viejo?'",
          rol: "Encargado de Diversión",
          imagen: "./pictures/team/bugs.jpg", 
        },
      ],
    } 
  }
}
</script>