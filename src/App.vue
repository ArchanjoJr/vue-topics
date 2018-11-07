<template>
  <div id="app">
    <p>Novo curso:
      <input type="text" v-model="novo" @keyup.enter="incluir">
        <button @click="incluir">Inserir</button>
    </p>
    <ul>
      <li v-for="curso in cursos" :key="curso.id"> {{ curso.nome }} </li>    
    </ul>
  </div>
</template>

<script>
import CursoItem from './components/CursoItem';
 export default {
 name: 'app',
 components: {
      CursoItem
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
