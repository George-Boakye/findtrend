<template>
    <button>{{ text }}</button>
</template>

<script>
export default {
    name: 'Button',
    props: ['text']
}
</script>

<style>
button {
    width: 129px;
    height: 42px;
    background: #FFFFFF;
    border-radius: 40px;
    cursor: pointer;
}
</style>