<template>
    <Container>
        <div>
            <header>
                <h2>Hello 👋</h2>

                <img src="../assets/profile.jpg" alt="">
            </header>
            
            <p>{{ $root.biography }}</p>
        </div>

    </Container>
</template>

<script>
import Container from './Container.vue'

export default {
    name: 'BiographySmall',
    components: { Container }
}
</script>

<style scoped>
header {
    display: flex;
    justify-content: space-between;
    align-items: center;

}

div {
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 2em;
    max-width: 600px;
}

img {
    border-radius: 50%;
    object-fit: cover;
    height: 6em;
    width: 6em;
    filter: grayscale();
}

p {
    
}
</style>