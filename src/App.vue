<template>
  <div id="app">
    <numeros></numeros>
  </div>
</template>

<script>
import Numeros from './components/Numeros.vue';
 export default {
 name: 'app',
 components: {
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
    incluir() {
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
