<template>
    <div>
        <p>El nombre es: {{nombre}}</p>
        <p>La edad es: {{edad}}</p>
    </div>
</template>

<script>
export default {
    name: 'Persona',
    props: [
        'nombre', 
        'edad'
    ]
}
</script>

<style scoped>

</style>