<template>
    <section>
        <slot></slot>
    </section>
</template>

<script>
    export default {
        name: 'Container',
        props: ['maxWidth']
    }
</script>

<style scoped>
section {
    display: flex;
    gap: 2em;
    align-items: center;

    border: 1px solid #333333;
    border-radius: 1em;
    padding: 2em;

    background-color: rgba(255, 255, 255, 0);
    backdrop-filter: blur(3px);

    transition: .3s;

    width: fit-content;

}

section:hover {
    transform: translateY(-5px);
}
</style>