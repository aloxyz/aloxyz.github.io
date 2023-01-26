<template>
    <Container>
        <div>
            <div>
                <h2>Hello 👋</h2>
            <p>{{ $root.biography }}</p>
            </div>

            <img src="../assets/profile.jpg" alt="">
        </div>

    </Container>
</template>

<script>
import Container from './Container.vue'

export default {
    name: 'Biography',
    components: { Container }
}
</script>

<style scoped>
div {
    display: flex;
    flex-direction: row;
    justify-content: center;
    gap: 2em;
}

div > div {
    display: flex;
    flex-direction: column;
    width: 16em;
}



img {
    border-radius: 1em;
    object-fit: cover;
    height: 100%;
    width: 16em;
    filter: grayscale();
    margin-left: 2em;
}

</style>