<template>
    <Header />

    <main class="dotBg">
        <BiographySmall />
        <Skills />
        <Links />
    </main>

    <Footer />
</template>

<script>
import Header from './Header.vue';
import BiographySmall from './BiographySmall.vue';
import Skills from './Skills.vue';
import Links from './Links.vue';
import Footer from './Footer.vue';

export default {
    name: 'MainSmall',

    components: {
        BiographySmall,
        Skills,
        Links,
        Header,
        Footer
    },
    
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