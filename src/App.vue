<template>
  <div id="app">
    <p>Novo curso:
      <input type="text" v-model="novo" @keyup.enter="incluir">
        <button @click="incluir">Inserir</button>
        <button @click="excluir">Excluir</button>
    </p>
    <ul>
      <li v-for="curso in cursos" :key="curso.id"> {{ curso.nome }} </li>    
    </ul>
    <br/> <numeros></numeros>
  </div>
</template>

<script>
import CursoItem from './components/CursoItem';
import Numeros from './components/Numeros.vue';
 export default {
 name: 'app',
 components: {
      CursoItem,
      Numeros,
 },
 data() {
    return {
          cursos: [
            { nome: 'ADS'},
            { nome: 'Banco de Dados'}
          ]
        }
      },

  methods: {
    incluir(event) {
      if(this.novo.trim().length == 0) {
        alert('O nome do curso deve ser preenchido!')
      }
      else {
        this.cursos.push( { nome: this.novo } );
      }
    },
    excluir(indice) {
      this.cursos.splice(indice, 1);
    }
  }
}
</script>

<style>

</style>
