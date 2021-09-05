<template>
    <header>{{ text }}</header>
</template>

<script lang="ts">
export default {
    name: 'TheHeader',
    props: {
        text: {
            type: String,
            default: 'kokoko'
        }
    }
}
</script>
<style scoped>
header {
    width: 100%;
    height: 60px;
    text-align: center;
    background: cornflowerblue;
}
</style>