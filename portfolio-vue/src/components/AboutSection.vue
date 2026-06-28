<script setup lang="ts">

</script>

<template>
    <section class="about" id="about">
        <div class="container">
            <div class="intro-text">
                <h2>
                Om meg
                </h2>
                <p class="intro">
                    Jeg heter Kamilla Selnes, er 29 år og kommer fra vakre Balsfjord i Nord-Norge. <span class="dialect">(Æ e altså ekte nordlending)</span>
                </p>
                <p>
                    Da jeg var liten lagde jeg min aller første nettside på piczo, før jeg gikk videre til å lage kule design på minstall, og til slutt endte opp med å lage min egne blogg på tumblr.
                    Gjennom alle disse årene har koding alltid fascinert meg, men det har bare blitt med tanken. Jeg er ikke spesielt glad i matte, og trodde man måtte være dritgod i det for å kunne lære seg å kode.
                </p>
                <p>
                    I min forrige jobb, jobbet jeg som møtebooker en stund, og der hørte jeg om GET Academy. Det var akkurat som om en ny verden åpnet seg for meg, da jeg forstod at jeg kunne begynne å kode, uten å være et mattegeni!!
                </p>    
                <p>
                    Jeg søkte, kom inn, og siden det har jeg lært meg vanvittig mye gøy og interessant.
                    Ikke bare har jeg lært hvordan man koder, men jeg har også lært å kjenne meg selv bedre - både på godt og vondt. Det høres veldig klisjé ut, men det er faktisk sant. 
                </p>
            </div>
        </div>
    </section>
</template>

<style scoped>
.about {
    position: relative;
    overflow: hidden;

    padding: 5rem 8vw 6rem;

    background: var(--bg-main);
}

.container {
    position: relative;

    max-width: 1200px;
    margin: 0 auto;
}

.intro-text {
    max-width: 720px;
    margin: 0 auto;
}

.about h2 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.5rem, 5vw, 4rem);

    margin-bottom: 1.25rem;
}

.about h2::after {
    content: "";

    display: block;

    width: 60px;
    height: 2px;

    margin-top: 0.6rem;

    background: var(--terracotta);
}

.intro-text p {
    font-family: 'Poppins', sans-serif;
    line-height: 1.8;

    margin-bottom: 1.2rem;
}

.dialect {
    display: block;

    margin-top: 0.5rem;

    font-size: 0.9rem;
    font-style: italic;

    color: var(--terracotta);
}
</style>
