<template>
    <div>
        <p>ID: {{id}}</p>
        <p>Nombre: {{name}}</p>
        <p>Email: {{email}}</p>
        <p>Tel: {{phone}}</p>
        <hr>
    </div>
</template>

<script>
export default {
    name: 'Usuarios',
    props: {
        id: Number,
        name: String,
        email: String,
        phone: String
    }
}
</script>