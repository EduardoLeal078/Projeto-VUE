<template>
    <h1>Componente Image</h1>
    {{ url }}
</template>

<script>
export default (await import('vue')).defineComponent({
    name: 'Image',
    props: {
        url: String
    },
    data() {
        return {
            msg: 'Estou no Image.vue',
        }
    }
})
</script>
    
<style></style>