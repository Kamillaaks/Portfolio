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
    <div class="skills-container">
        <div class="skills-list">
            <li class="skill-item"
                v-for="skill in skills"
                :key="skill.name"
                @mouseenter="selectedSkill = skill"
            >
                {{ skill.name }}
            </li>
        </div>
        

        <div class="skill-description">
            <h3>{{ selectedSkill.name }}</h3>
            <p>{{ selectedSkill.description }}</p>
        </div>
    </div>
   
</template>

<style scoped>
.skills-container {
    display: flex;
    justify-content: center;
    gap: 1.5rem;

    max-width: 700px;
    margin: 3rem auto;
}

.skills-list {
    width: 180px;

    background-color: var(--bg-main);

    border: 1px solid rgba(0, 0, 0, 0.08);
    border-radius: 8px;

    padding: 1.5rem;
}

.skill-description {
    width: 320px;
    min-height: 250px;

    background-color: var(--bg-main);

    border: 1px solid rgba(0, 0, 0, 0.08);
    border-radius: 8px;

    padding: 2rem;

    display: flex;
    flex-direction: column;
    justify-content: center;

    text-align: center;
}

.skill-item {
    list-style: none;
    cursor: pointer;

    transition: all 0.2s ease;
}

.skill-item:hover {
    transform: translateX(4px);
    color: var(--accent-burgundy);
}

.skill-description h3 {
    color: var(--accent-burgundy);

    margin-bottom: 1rem;

    font-size: 1.75rem;
}
</style>