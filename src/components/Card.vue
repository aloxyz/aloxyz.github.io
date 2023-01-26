<template>
    <div class="card">
        <header>
            <h3><slot name="header"></slot></h3>
        </header>

        <section>
            <slot name="content"></slot>
        </section>

        <footer>
            <slot name="footer"></slot>
        </footer>
    </div>
</template>

<script>
    export default {
        name: 'Card',
        props: ['borderColor', 'color']
    }
</script>

<style scoped>

.card {
    transition: .3s;
    

    display: flex;
    flex-direction: column;
    justify-content: space-between;

    border-radius: 1em;
    padding: 2em;
    margin: 1em 1em 1em 0em;
    border: 1px solid #333333;
    
    min-width: 18em;
    min-height: 18em;

    max-width: 18em;
    max-height: 20em;

    background-color: rgba(255, 255, 255, 0);
    backdrop-filter: blur(3px);
}

.card h3 {
    margin: 0;
}

.card:hover {
    transform: translateY(-5px);
}

section {
    margin: 1em 0
}

header {
    padding-bottom: 1em;
    border-bottom: solid 1px;
}

footer {
    display: flex;
    flex-wrap: wrap;
    gap: 1em;

    padding-top: 1em;
    border-top: solid 1px;
}


</style>