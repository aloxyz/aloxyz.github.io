<template>
    <footer>
        <h2>Contacts</h2>
        <ul>
            <li>
                <i class="fa-brands fa-linkedin fa-xl"></i>
                <a href="https://www.linkedin.com/in/aloxyz">LinkedIn</a>
            </li>


            <li>
                <i class="fa-solid fa-paper-plane fa-lg"></i>
                <a href="mailto:aloxyz@tuta.io">Email</a>
            </li>
        </ul>
    </footer>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
footer {
    border-top: solid 1px #333333;
    margin: 3em 1em 1em 1em;
    padding: 2em 1em 2em 1em;
}

footer > ul {
    display: flex;
    flex-direction: column;
    gap: 1em;
    margin-top: 1em;
}

footer i {
    margin-right: .4em;
}
</style>