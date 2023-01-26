<template>
    <section>
        <h2>{{ this.title }}</h2>
        <div class="heroSection">

            <Card v-for="card in this.cards">
                <template v-slot:header>
                    {{ card.title }}
                </template>

                <template v-slot:content>
                    {{ card.content }}
                </template>

                <template v-slot:footer>
                    <Button v-for="button in card.buttons"
                    :content="button.content"
                    :color="button.color"
                    :url="button.url"
                    >
                    </Button>

                </template>
            </Card>
        </div>
    </section>

</template>

<script>
import Card from './Card.vue'
import Button from './Button.vue'

export default {
    name: 'HeroSection',
    components: { Card, Button },
    props: ['title', 'color', 'cards']

}
</script>

<style scoped>
.heroSection {
    display: flex;
    justify-content: flex-start;
    border-radius: 1em;
}

</style>