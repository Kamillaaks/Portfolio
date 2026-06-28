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
.ongoing-projects {
    padding: 6rem 8vw;
    background: var(--bg-soft);
}

.ongoing-projects h2 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.5rem, 5vw, 4rem);
    text-align: center;

    margin-bottom: 1rem;
}

.ongoing-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1.5rem;

    max-width: 1000px;
    margin: 3rem auto 0;
}

.ongoing-card {
    display: block;

    min-height: 260px;
    padding: 2rem;

    background: var(--bg-main);
    border: 1px solid rgba(75, 38, 25, 0.18);

    text-decoration: none;
    color: var(--espresso);
}

.ongoing-card img {
    display: none;
}

.ongoing-overlay {
    height: 100%;

    display: flex;
    flex-direction: column;
    justify-content: center;

    text-align: left;
}

.ongoing-overlay h3 {
    font-family: 'Playfair Display', serif;
    font-size: 2rem;

    margin-bottom: 1rem;
}

.ongoing-overlay p {
    margin: 0;
    line-height: 1.8;
}
</style>