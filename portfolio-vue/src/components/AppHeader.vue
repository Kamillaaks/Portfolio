<script setup lang="ts">

</script>

<template>
    <header class="header">
        <h1 class="header-logo">
            <a href="#main" class="home">Kamilla</a>
        </h1>
        <nav>
            <ul class="header-links">
                <li>
                    <a href="https://github.com/Kamillaaks">
                        <img src="../assets/icons/github.svg" alt="Kamilla">
                    </a>
                </li>
                <li>
                    <a href="https://www.linkedin.com/in/kamilla-selnes-a55bb5117/">
                        <img src="../assets/icons/linkedin.svg" alt="Kamilla">
                    </a>
                </li>
                <li>
                    <a href="mailto:someone@example.com">
                        <img src="../assets/icons/email.svg" alt="Kamilla">
                    </a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style scoped>
.header {
    padding: 20px 20px;

    display: flex;
    align-items: center;
    justify-content: space-between;

    position: sticky;
    top: 0;
    z-index: 100;

    background-color: var(--accent-mustard);
}

.header-logo {
    margin: 0 auto;
}

.header-links {
    display: flex;
    flex-direction: row;
    gap: 0.7rem;
    list-style: none;
    margin: 0;
    padding: 0;
    align-items: center;
}

.header-links img {
    height: 30px;
    width: auto;
    vertical-align: middle;
    margin: 0 5px;
}

.home {
    color: #111;
    text-decoration: none;
}

.icon {
    height: 50px;
    width: auto;
    margin: 0 10px;
    vertical-align: middle;
}
</style>