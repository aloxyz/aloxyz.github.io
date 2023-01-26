<template>
    <Container>
        <div class="master" :style="{width: width}">
            <header>
                <h2>Links <i class="fa-solid fa-link"></i></h2>
            </header>

            <section class="content">
                    <div>
                        <Breadcrumb v-for="link in $root.links" :bgColor="$root.colors.orange">
                            
                            <a :href="link.url">{{ link.name }}</a>
                        </Breadcrumb>
                    </div>

            </section>
        </div>

    </Container>
</template>

<script>
import Container from './Container.vue';
import Breadcrumb from './Breadcrumb.vue';

export default {
    name: 'Links',
    props: ['width'],
    components: { Container, Breadcrumb },

    data() {
        return {
        }

    }

}
</script>

<style scoped>

.master {
    display: flex;
    flex-direction: column;
    gap: 2em;
}

.content {
    display: flex;
    flex-direction: column;
    gap: 2em;
}

div {
    margin-top: .3em;
    display: flex;
    gap: .5em;
    flex-wrap: wrap;
}

div > div:hover {
    filter: brightness(115%);
    transition: .3s;

}

a:hover {
    transition: .3s;
    color: #333333;
    
}

</style>