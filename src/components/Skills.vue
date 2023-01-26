<template>
    <Container>
        <div class="master" :style="{width: width}">
            <header>
                <h2>Skills <i class="fa-solid fa-gear"></i></h2>
            </header>

            <section class="content">
                <section>
                    <h3>Technologies</h3>
                    <div>
                        <Breadcrumb v-for="skill in $root.skills.tech" :bgColor="$root.colors.blue">
                            {{ skill }}
                        </Breadcrumb>
                    </div>
                </section>

                <section>
                    <h3>Audio</h3>
                    <div>
                        <Breadcrumb v-for="skill in $root.skills.audio" :bgColor="$root.colors.red">
                            {{ skill }}
                        </Breadcrumb>
                    </div>
                </section>


                <section>
                    <h3>Graphics</h3>
                    <div>
                        <Breadcrumb v-for="skill in $root.skills.graphics" :bgColor="$root.colors.green">
                            {{ skill }}
                        </Breadcrumb>
                    </div>
                </section>
            </section>
        </div>

    </Container>
</template>

<script>
import Container from './Container.vue';
import Breadcrumb from './Breadcrumb.vue';

export default {
    name: 'Skills',
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

</style>