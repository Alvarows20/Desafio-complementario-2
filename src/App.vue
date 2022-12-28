<template>
  <div id="app">
    <AppHeader :tittle="tittle" :subtittle="subtittle"/>
    <AppTables :tittle="one.tittle" :description="one.description" :participants="one.participants" :styles="one.styles"/>
    <AppTables :tittle="two.tittle" :description="two.description" :participants="two.participants" :styles="two.styles"  />
    <AppTables :tittle="three.tittle" :description="three.description" :participants="three.participants" :styles="three.styles"/>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import AppTables from './components/AppTables.vue';

export default {
  name: 'App',
  components: {
    AppHeader, AppTables,
  },
  data() {
    return {
      tittle:"Junta Federal de Jóvenes Industriales Argentinos",
      subtittle:"Autoridades destacadas",
      one: {
        tittle: "Día 1",
        description: "Visita a empresas de la ciudad",
        participants: [
          {name: "Juan", surname: "González", organisation: "CCIRR", arrival: new Date("2022/05/05").toLocaleDateString()},
          {name: "José", surname: "Dellepiane", organisation: "CICAE", arrival: new Date("2022/05/05").toLocaleDateString()},
          {name: "Rosana", surname: "Júarez", organisation: "FISFE", arrival: new Date("2022/05/04").toLocaleDateString()},
          {name: "Pedro", surname: "Dellasanta", organisation: "CCIRR", arrival: new Date("2022/05/05").toLocaleDateString()},
          {name: "Evangelina", surname: "Ramírez", organisation: "UIA", arrival: new Date("2022/05/04").toLocaleDateString()},
          ],
        styles: "day-one",
      },
      two: {
        tittle: "Día 2",
        description: "Encuentro de jóvenes empresarios",
        participants: [
          {name: "Mariano", surname: "Lufiego", organisation: "UIA", arrival: new Date("2022/05/05").toLocaleDateString()},
          {name: "Laura", surname: "Tapia", organisation: "FISFE", arrival: new Date("2022/05/05").toLocaleDateString()},
          {name: "Santiago", surname: "Milanese", organisation: "CICAE", arrival: new Date("2022/05/06").toLocaleDateString()},
          {name: "Iván", surname: "López", organisation: "CCIRR", arrival: new Date("2022/05/06").toLocaleDateString()},
          {name: "Mauro", surname: "Martínez", organisation: "CCIRR", arrival: new Date("2022/05/06").toLocaleDateString()},
          ],
        styles: "day-two",
      },
      three: {
        tittle: "Día 3",
        description: "Charla debate sobre actualidad industrial",
        participants: [
          {name: "Mariana", surname: "Lombardo", organisation: "CICAE", arrival: new Date("2022/05/07").toLocaleDateString()},
          {name: "Guillermina", surname: "Fernández", organisation: "CICAE", arrival: new Date("2022/05/07").toLocaleDateString()},
          {name: "Carolina", surname: "Allasino", organisation: "UIA", arrival: new Date("2022/05/06").toLocaleDateString()},
          {name: "Diego", surname: "Pérez", organisation: "FISFE", arrival: new Date("2022/05/06").toLocaleDateString()},
          {name: "Adolfo", surname: "Daniele", organisation: "CCIRR", arrival: new Date("2022/05/07").toLocaleDateString()},
          ],
        styles: "day-three",
      },
    }
  },
}
</script>

<style>

  * {
    font-family: Verdana, Geneva, Tahoma, sans-serif;
  }

  #app {
    margin-top: 20px;
    margin-left: 20px;
  }
  
</style>
