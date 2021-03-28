<template>
    <div>
        <h1 style="color: red">
            Componente
            <hr>
            <slot>
                Esto se sobreescribe
            </slot>
            <br>
            <slot>
                Esto también
            </slot>
            <br>
            <slot name="slotNombrado">
                Este slot se sobreescribe con nombre
            </slot>
        </h1>
    </div>
</template>

<script>
export default {
    name: 'CompSlot'
}
</script>
