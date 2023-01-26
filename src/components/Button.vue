<template>
        <button v-html="content" 
        :style="{backgroundColor: this.color}"
        :href="url"
        >
        </button>
</template>

<script>
    
    export default {
        name: 'Button',
        props: ['url', 'color', 'content']
    }
</script>

<style scoped>
    button > * {
        margin: 0;
    }
    button {
        max-height: 3em;
        padding:  1em;
        padding-bottom: 2.3em;

        border: none;

        border-radius: .6em;
        color: white;
    }
    
    button:hover {
        transition: .3s;
        cursor: pointer;
        filter: brightness(120%);
    }
    </style>