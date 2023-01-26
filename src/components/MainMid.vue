<template>
    <Header />

    <main class="dotBg">
        <Biography />
        <Skills/>
        
        <Links /> 
    </main>

    <Footer />
</template>

<script>
import Header from './Header.vue';
import Biography from './Biography.vue';
import Skills from './Skills.vue';
import Links from './Links.vue';
import Footer from './Footer.vue';

export default {
    name: 'MainMid',

    components: {
        Biography,
        Skills,
        Links,
        Header,
        Footer
    },

    data() {

    }
    
}
</script>

<style scoped>

main {
    display: flex;
    flex-direction: column;
    justify-items: center;
    align-items: center;
    gap: 5em;
    padding: 3em 1em 3em 1em;
}

</style>