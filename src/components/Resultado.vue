<template>
    <div id='resul'>
        <b> {{parseInt(a) + parseInt(b)}}</b><br/>
        <b> {{a - b}}</b><br/>
        <b> {{a * b}}</b>
    </div>
</template>
<script>

export default {
    name: 'Resultado',
    props : {
        a: Number,
        b: Number,
    }
}
</script>
