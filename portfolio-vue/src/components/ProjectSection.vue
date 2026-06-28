<script setup lang="ts">
import {ref, computed} from 'vue'
import ArrowLeft from '../assets/icons/arrowLeft.svg'
import ArrowRight from '../assets/icons/arrowRight.svg'

const projects = [
    {
        title: 'Mood Tracker',
        image: '',
        link: '#',
    },
     {
        title: 'Mini Trello',
        image: '',
        link: '#',
    },

]

const currentProjectIndex = ref(0)

const currentProject = computed(() => {
    return projects[currentProjectIndex.value]
})

function nextProject() {
    currentProjectIndex.value++

    if (currentProjectIndex.value >= projects.length) {
        currentProjectIndex.value = 0
    }
}

function prevProject() {
    currentProjectIndex.value--

    if (currentProjectIndex.value < 0) {
        currentProjectIndex.value = projects.length - 1
    }
}
</script>

<template>
    <section id="projects" class="projects-section">
        <h2 class="projects-title">
            Mine prosjekter
        </h2>
        <p class="projects-intro">
            Prosjekter jeg har bygget gjennom studiet og på fritiden
        </p>

        <div class="project-carousel">
            <button class="arrow-btn arrow-btn-left" @click="prevProject">
                <ArrowLeft class="arrow-icon" />
            </button>

            <a :href="currentProject.link" class="project-card">
                <h3>
                    {{ currentProject.title }}
                </h3>
            </a>

            <button class="arrow-btn arrow-btn-right" @click="nextProject">
                <ArrowRight class="arrow-icon" />
            </button>
        </div>
    </section>
</template>

<style scoped>
.projects-section {
    padding: 6rem 8vw;
    background: var(--bg-soft);
}

.projects-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.5rem, 5vw, 4rem);
    text-align: center;

    margin-bottom: 1rem;
}

.projects-intro {
    max-width: 620px;

    margin: 0 auto 2.5rem;

    text-align: center;

    font-family: 'Poppins', sans-serif;
    font-size: 1.1rem;
    line-height: 1.8;

    color: var(--espresso);

    opacity: 0.8;
}

.project-carousel {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 2rem;

    max-width: 700px;
    margin: 0 auto;
}

.project-card {
    width: 420px;
    min-height: 140px;

    display: flex;
    align-items: center;
    justify-content: center;

    text-decoration: none;
    color: var(--espresso);

    background: var(--bg-main);
    border: 1px solid rgba(75, 38, 25, 0.18);
    border-radius: 0;

    box-shadow: 0 18px 45px rgba(75, 38, 25, 0.08);
}

.project-card h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.4rem;
    text-align: center;
}

.arrow-btn {
    display: flex;
    justify-content: center;
    align-items: center;

    padding: 0;

    background: transparent;
    border: none;

    cursor: pointer;
}

.arrow-icon {
    width: 36px;
    height: 36px;

    color: var(--espresso);
}
</style>