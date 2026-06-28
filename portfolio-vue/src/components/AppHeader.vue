<script setup lang="ts">
import LogoSun from '../assets/icons/sol.svg'
import GithubIcon from '../assets/icons/github.svg'
import LinkedinIcon from '../assets/icons/linkedin.svg'
import EmailIcon from '../assets/icons/email.svg'
</script>

<template>
    <header class="header">
        <a href="#main" class="header-logo">
            <span>Kamilla</span>
            <LogoSun class="logo-sun"/>
            <span>Selnes</span>
        </a>
        
        <nav>
            <ul class="header-links">
                <li>
                    <a href="https://github.com/Kamillaaks">
                        <GithubIcon class="icon" />
                    </a>
                </li>

                <li>
                    <a href="https://www.linkedin.com/in/kamilla-selnes-a55bb5117/">
                        <LinkedinIcon class="icon" />
                    </a>
                </li>

                <li>
                    <a href="mailto:...">
                        <EmailIcon class="icon" />
                    </a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style scoped>
.header {
    padding: 0.35rem 8vw;

    display: flex;
    justify-content: space-between;
    align-items: center;

    position: sticky;
    top: 0;
    z-index: 100;

    background-color: var(--bg-main);
    background-image: url("../assets/textures/groovepaper.png");
    background-repeat: repeat;
    background-size: auto;
}

.header-logo {
    display: flex;
    align-items: center;
    gap: 0.65rem;

    text-decoration: none;
    color: var(--espresso);

    font-family: "Playfair Dislpay", serif;
    text-transform: uppercase;
    letter-spacing: 0.22rem;
}

.logo-sun {
    width: 26px;
    height: 26px;

    flex-shrink: 0;

    color: var(--golden-hour);
}

.header-links {
    display: flex;
    flex-direction: row;
    gap: 1.2rem;
    list-style: none;
    margin: 0;
    padding: 0;
    align-items: center;
}

.header-links a {
    color: var(--espresso);
}

.header-links a:hover {
    color: var(--terracotta);
}

.home {
    color: #111;
    text-decoration: none;
}

.icon {
    width: 26px;
    height: auto;
}
</style>