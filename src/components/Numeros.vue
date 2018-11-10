<template>
    <div id='num'>
        <input v-model="num1" type='number'> <input v-model="num2" type='number'><br/>
        <resultado :a='num1' :b='num2'></resultado>
    </div>
</template> 
<script>
import Resultado from './Resultado.vue';
export default {
    name: 'Numeros',
    components:{
        Resultado,
    },
    data(){
        return {
            num1: 0,
            num2: 0,
        }
    }
}
</script>
