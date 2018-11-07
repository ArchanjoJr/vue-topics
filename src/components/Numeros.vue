<template>
    <div id='num'>
        <input v-model="num1" type='text'><br/>
        <input v-model="num2" type='text'><br/>
        <button @click="add">adicionar </button><br/>
        <button @click="subtr">subtrair</button><br/>
        <button @click="multp">multiplicacao</button><br/><br/>
        <resultado></resultado>
    </div>
</template>
<script>
import Resultado from './Resultado.vue';
export default {
    name: 'Numeros',
    components:{
        Resultado,
    },
    methods:{
        add(){
            alert(parseInt(this.num1)+parseInt(this.num2));
        },
        subtr(){
            alert(parseInt(this.num1)-parseInt(this.num2));
        },
        multp(){
            alert(parseInt(this.num1)* parseInt(this.num2));
        },
    }
}
</script>
