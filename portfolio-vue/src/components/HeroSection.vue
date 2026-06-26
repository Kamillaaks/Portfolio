<script setup lang="ts">
import ZebraPattern from '../assets/icons/zebra.svg'
</script>

<template>
    <section class="hero">
        <div class="hero-text">
            <div class="hero-inner">
                <h1>
                    Hei, jeg er Kamilla.
                </h1>

                <p class="intro">
                    Jeg liker å bygge apper hvor design og kode går hånd i hånd. Jeg liker å skape løsninger
                    som både fungerer godt og føles gode å bruke.
                </p>

                <p>
                    Jeg trives best når jeg får kombinere det visuelle med det tekniske,
                    og når jeg kan utvikle prosjekter som føles gjennomtenkte
                    og personlige.
                </p>

                <a href="#projects" class="button">
                    Se prosjekter
                </a>
            </div>
        </div>

        <div class="hero-img">
            <ZebraPattern class="zebra-pattern"/>
            <img 
                src="../assets/images/Kamilla.jpg" 
                alt="Kamilla"
                class="portrait"
            >
   
        </div>
    </section>
</template>

<style scoped>
.hero {
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    gap: 4rem;

    min-height: 90vh;
    padding: 4rem 8vw;

    background: var(--bg-soft);
}

.hero-text {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 3rem;
}

.hero h1 {
    font-size: 3.5rem;
    margin-bottom: 0.8rem;
}

.hero-text h1 {
    font-family: 'Playfair Display', serif;
}

.hero-text p {
    line-height: 1.6;
    margin-bottom: 1.8rem;
}

.hero-inner {
    max-width: 400px;
}

.hero-img {
    position: relative;

    display: flex;
    justify-content: center;
    align-items: center;
}

.portrait {
    position: relative;
    z-index: 2;

    width: 300px;
    max-height: 100%;
    border-radius: 72% 44% 31% 56% / 39% 37% 66% 27%;
}

.zebra-pattern {
    position: absolute;

    width: 500px;

    left: 50%;
    top: 50%;

    transform: translate(-55%, -50%);
    border-radius: 78% 35% 20% 31% / 40% 29% 52% 49%;

    z-index: 1;

    color: var(--bg-card-dark);
    opacity: 0.5;
}
</style>