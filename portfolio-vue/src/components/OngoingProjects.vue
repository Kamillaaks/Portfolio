<script setup lang="ts">
    const ongoingProjects = [
        {
            title: 'Outfit Repeater',
            description: 'En appidé for å lagre antrekk og finne inspirasjon i egne outfits',
            image: '',
            link: '#',
        },

    ]
</script>

<template>
    <section class="ongoing-projects">
        <h2>Pågående prosjekter</h2>

        <div class="ongoing-grid">
            <a
                v-for="project in ongoingProjects"
                :key="project.title"
                :href="project.link"
                class="ongoing-card"
            >
                <img :src="project.image" :alt="project.title">

                <div class="ongoing-overlay">
                    <h3>{{ project.title }}</h3>
                    <p>{{ project.description }}</p>
            </div>
            </a> 
        </div>
    </section>
</template>

<style scoped>
.ongoing-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 1.5rem;

    max-width: 1000px;
    margin: 3rem auto;
    padding: 0 2rem;
}

.ongoing-card {
    position: relative;
    display: block;

    aspect-ratio: 4 / 3;
    overflow: hidden;

    border-radius: 10px;
    text-decoration: none;
    color: var(--text-main);
}

.ongoing-card img {
    width: 100%;
    height: 100%;
    object-fit: cover;

    transition: filter 0.25s ease, transform 0.25s ease;
}

.ongoing-overlay {
    position: absolute;
    inset: 0;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    padding: 1.5rem;
    text-align: center;

    opacity: 0;
    transition: opacity 0.25s ease;
}

.ongoing-card:hover img {
    filter: brightness(1.15) opacity(0.35);
    transform: scale(1.03);
}

.ongoing-card:hover .ongoing-overlay {
    opacity: 1;
}
</style>