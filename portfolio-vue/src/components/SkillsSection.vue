<script setup lang="ts">
import {ref} from 'vue'

const skills = [
    {
        name: 'HTML',
        description:  'Kan bygge semantiske nettsider med riktig struktur, lenker, skjemaer og fokus på tilgjengelighet.',
    },
    {
        name: 'CSS',
        description: 'Kan lage responsive layouts med Flexbox og Grid, bruke CSS-variabler, media queries, animasjoner og moderne styling.',
    },
    {
        name: 'JavaScript',
        description: 'Kan manipulere DOM-en, håndtere events, bruke funksjoner, løkker, arrays og objekter for å lage interaktive nettsider.',
    },
    {
        name: 'TypeScript',
        description: 'Kan bruke typer, interfaces og typekontroll for å skrive mer robust og vedlikeholdbar kode.'
    },
    {
        name: 'C#',
        description: 'Har jobbet med grunnleggende programmering i C# gjennom studier og praktiske oppgaver.'
    },
    {
        name: 'Vue',
        description: 'Kan bygge komponentbaserte applikasjoner med Vue 3, Composition API, props, emits, v-for, v-if og reaktiv state.'
    },
    {
        name: 'Pinia',
        description: 'Kan bruke Pinia til state management og dele data mellom komponenter i Vue-applikasjoner.'
    },
    {
        name: 'Nuxt',
        description: 'Har erfaring med filbasert routing, layouts og prosjektstruktur i Nuxt 4 gjennom teamprosjekter.'
    },
    {
        name: 'Git & GitHub',
        description: 'Kan bruke Git til versjonskontroll, opprette repositories, gjøre commits, pushe endringer og samarbeide via GitHub.'
    },
    {
        name: 'Responsive Design',
        description: 'Kan tilpasse nettsider til mobil, nettbrett og desktop ved hjelp av fleksible layouts og media queries.'
    },
    {
        name: 'Tilgjengelighet',
        description: 'Har kunnskap om semantisk HTML, tastaturnavigasjon og grunnleggende WCAG-prinsipper for universell utforming.'
    },
]

const selectedSkill = ref(skills[0])
</script>

<template>
    <section id="skills" class="skills-section">
        <h2 class="skills-title">
            Ferdigheter
        </h2>

        <p class="skills-intro">
            Teknologier og verktøy jeg har jobbet med gjennom studiet og egne prosjekter.
        </p>

        <div class="skills-container">
            <ul class="skills-list">
                <li
                    v-for="skill in skills"
                    :key="skill.name"
                    class="skill-item"
                    @mouseenter="selectedSkill = skill"
                >
                    {{ skill.name }}
                </li>
            </ul>

            <div class="skill-description">
                <h3>
                    {{ selectedSkill.name }}
                </h3>

                <p>
                    {{ selectedSkill.description }}
                </p>
            </div>
        </div>
    </section>
</template>

<style scoped>
.skills-section {
    margin-top: 4rem;
    padding: 6rem 8vw;
    background: var(--bg-main);
}

.skills-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.5rem, 5vw, 4rem);
    text-align: center;
    margin-bottom: 3rem;
    color: var(--espresso);
}

.skills-container {
    display: flex;
    justify-content: center;
    align-items: stretch;
    gap: 1.5rem;

    max-width: 1100px;
    margin: 0 auto;
}

.skills-intro {
    max-width: 620px;
    margin: 0 auto 2rem;
    text-align: center;
    line-height: 1.8;
    color: var(--espresso);
    opacity: .8;
}

.skills-list,
.skill-description {
    background: var(--bg-dark);
    color: var(--text-light);
    border: 1px solid rgba(75, 38, 25, 0.14);
}

.skills-list {
    width: 300px;
    padding: 2rem;

    list-style: none;
    margin: 0;
}

.skill-item {
    cursor: pointer;
    font-size: 1.05rem;
    line-height: 1.9;

    transition:
        color 0.2s ease,
        transform 0.2s ease;
}

.skill-item:hover {
    transform: translateX(6px);
    color: var(--terracotta);
}

.skill-description {
    width: 600px;
    min-height: 330px;

    padding: 2.25rem;

    display: flex;
    flex-direction: column;
    justify-content: center;

    text-align: center;
}

.skill-description h3 {
    font-family: 'Playfair Display', serif;
    font-size: 2.8rem;

    color: var(--text-light);

    margin-bottom: 1.5rem;
}

.skill-description p {
    font-size: 1.05rem;
    line-height: 1.8;

    color: var(--text-light);
}
</style>