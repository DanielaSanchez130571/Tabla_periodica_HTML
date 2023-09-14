<script setup>
defineProps({
    numero: String,
    nombre: String,
    grupo: String,
})

</script>
<template>
    <h1>.</h1>
    <div>
        <h1> {{ numero }} - {{ nombre }} - {{ grupo }}</h1>
    </div>
</template>