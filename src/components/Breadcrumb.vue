<template>
    <div :style="{
            backgroundColor: this.bgColor,
            color: this.color
        }">
        <slot/>
    </div>
</template>

<script>
    export default {
        name: 'Breadcrumb',
        props: ['bgColor', 'color']
    }
</script>

<style scoped>
    div {
        font-size: .9em;

        max-height: 3em;
        padding:  .5em;

        border: none;

        border-radius: .5em;
        color: white;

        width: max-content;

    }
</style>