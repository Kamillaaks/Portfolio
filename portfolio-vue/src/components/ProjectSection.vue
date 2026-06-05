<script setup lang="ts">
import {ref, computed} from 'vue'
import arrowLeft from '../assets/icons/arrow-left.svg'
import arrowRight from '../assets/icons/arrow-right.svg'

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
        <div class="project-carousel">
             <button class="arrow-btn" @click="prevProject">
            <img :src="arrowLeft" alt="Forrige prosjekt">
            </button>
            <div class="projects-grid">
            <a :href="currentProject.link" class="project-card">
                <h3>
                    {{ currentProject.title }}
                </h3>
            </a>
        </div>
        <button class="arrow-btn" @click="nextProject">
            <img :src="arrowRight" alt="Neste prosjekt">
        </button>
        </div>
       

    </section>
</template>

<style scoped>
.arrow-btn {
    background: transparent;
    border: none;
    cursor: pointer;
    padding: 0;
}

.arrow-btn img {
    width: 48px;
    height: 48px;
    transition: transform 0.2s ease;
}

.arrow-btn:hover img {
    transform: scale(1.1);
}

.project-carousel {
    display: grid;
    grid-template-columns: auto 1fr auto;
    align-items: center;
    max-width: 900px;
    margin: 0 auto;
}
.projects {
    padding: 50px 20px;
    max-width: 1200px;
    margin: 0 auto;
}

.projects-title {
    text-align: center;
    font-size: 2rem;
    margin-bottom: 40px;
}

.projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
}

/* .projects-grid img{
    height: 40rem;
    width: auto;
    object-fit: cover;
    display: block;
} */

.project-card {
    text-decoration: none;
    color: inherit; /* Tvinger teksten til å få samme farge fra sitt direkte overordnede element */
    overflow: hidden;
}

.project-card img {
    height: 40rem;
    width: 100%; 
    object-fit: cover;
    border-radius: 8px;
}

.project-card h3 {
    text-align: center;
    padding: 15px;
}

</style>