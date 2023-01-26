<template>
    <header>
        <div> <!-- div needed for the typewriter effect -->
            <h1>Gabriele Aloisio</h1>
            <div class="typewriter">
                <p>Coding like a musician.</p>
            </div>
        </div>

        <!-- <ul>
            <li><a href="#projects">Projects</a></li>
            <li><a href="">Links</a></li>
        </ul> -->
    </header>
</template>

<script>
    export default {
        name: 'Header'
    }
</script>

<style scoped>
header {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: flex-start;
    /* padding: 0em 16em 4em 16em; */
    padding: 1em 1em 3em 1em;
}

/* header links */
header ul {
    display: flex;
    flex-direction: row;
    gap: 2em;
    margin: 0 auto 0 auto;
}

header a {
    font-size: 22px;
    font-weight: 600;
}
</style>