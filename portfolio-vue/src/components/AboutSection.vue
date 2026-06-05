<script setup lang="ts">

</script>

<template>
    <section class="about">
        <div class="wave wave-top"></div>

        <div class="container">
            <div class="intro-text">
                <h2>
                Om meg
                </h2>
                <p class="intro">
                    Jeg heter Kamilla Selnes, er 29 år og kommer fra vakre Balsfjord i Nord-Norge. (Æ e altså ekte nordlending)
                </p>
                <p>
                    Da jeg var liten lagde jeg min aller første nettside på piczo, før jeg gikk videre til å lage kule design på minstall, og til slutt endte opp med å lage min egne blogg på tumblr. <br>
                    Gjennom alle disse årene har koding alltid fascinert meg, men det har bare blitt med tanken. Jeg er ikke spesielt glad i matte, og trodde man måtte være dritgod i det for å kunne lære seg å kode. <br>
                    I min forrige jobb, jobbet jeg som møtebooker en stund, og der hørte jeg om GET Academy. Det var akkurat som om en ny verden åpnet seg for meg, da jeg forstod at jeg kunne begynne å kode, uten å være et mattegeni!! <br>
                    Jeg søkte, kom inn, og siden det har jeg lært meg vanvittig mye gøy og interessant.
                    Ikke bare har jeg lært hvordan man koder, men jeg har også lært å kjenne meg selv bedre - både på godt og vondt. Det høres veldig klisjé ut, men det er faktisk sant. 
                    Jeg lærer HTML, CSS, JavaScript, Typescript, og har også vært innom C#. Jeg trives veldig godt med alle disse språkene, og gleder meg til å lære enda mer! 
                </p>
            </div>
        </div>

        <div class="wave wave-bot"></div>
    </section>
</template>

<style scoped>
.about {
    position: relative;
    overflow: hidden;
    padding-top: 100px;    /* plass til toppbølge */
    padding-bottom: 100px; /* plass til bunnbølge */
}

.container {
    position: relative;
    max-width: 100%;
    margin: 0 auto;
    background-color: var(--accent-sage);
    z-index: 2; /* ligger over bølgene */
    padding: 20px;
}

.intro-text {
    max-width: 700px;
    margin-left: auto;
    margin-right: auto;
}

.wave {
    position: absolute;
    width: 100%;
    height: 100px;
    left: 0;
    background-color: var(--accent-sage);

    mask-image: url('../assets/icons/wave.svg');
    mask-size: cover;
    mask-repeat: no-repeat;
    mask-position: center;

    -webkit-mask-image: url('../assets/icons/wave.svg');
    -webkit-mask-size: cover;
    -webkit-mask-repeat: no-repeat;
    -webkit-mask-position: center;

    z-index: 1; /* bak containeren */
}

.wave-top {
    top: 0;
    
}

.wave-bot {
    bottom: 0;
    transform: rotate(180deg);
}

</style>
