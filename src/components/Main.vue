<template>
    <Header />

    <main class="dotBg">
        <div class="leftCol">
            <Skills width="24.7em"/>
        </div>

        <div class="rightCol">
            <Biography />
            <Links width="29.3em"/> 
        </div>
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
    name: 'Main',

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
    justify-content: center;
    gap: 5em;
    padding: 3em 1em 3em 1em;
}

div {
    display: flex;
    flex-direction: column;
    gap: 5em;
    justify-content: centerr;
}

.leftCol {
    margin-top: 10em;
}

</style>