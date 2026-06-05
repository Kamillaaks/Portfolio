<script setup lang="ts">

</script>

<template>
    <section class="hero">
        <div class="hero-text">
            <div class="hero-inner">
                <h1>
                    Hei, jeg er Kamilla.
                </h1>

                <p class="intro">
                    Jeg lærer å bygge nettsider og digitale løsninger med fokus
                    på struktur, estetikk og funksjon.
                </p>

                <p>
                    Jeg trives best når jeg får kombinere det visuelle med det tekniske,
                    og når jeg kan utvikle prosjekter som føles gjennomtenkte
                    og personlige.
                </p>

                <a href="#projects" class="cta-button">
                    Se prosjekter
                </a>
            </div>
        </div>

        <div class="hero-img">
            <img src="../assets/images/Kamilla.jpg" alt="Kamilla">
        </div>
    </section>
</template>

<style scoped>
.hero {
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding: 4rem 2rem;
}

.hero-text {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 3rem;
}

.hero-text h1 {
    font-family: 'Cooper Black', serif;
}

.hero-text p {
    line-height: 1.6;
}

.hero-text-inner {
    max-width: 400px;
}

.hero-img {
    width: 500px;
    aspect-ratio: 1/1;

    mask-image: url('../assets/icons/flower.svg');
    mask-size: contain;
    mask-repeat: no-repeat;
    mask-position: center;

    -webkit-mask-image: url('../assets/icons/flower.svg');
    -webkit-mask-size: contain;
    -webkit-mask-repeat: no-repeat;
    -webkit-mask-position: center;
}

.hero-img img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>