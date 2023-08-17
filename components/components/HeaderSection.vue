<template>
    <section>
        <header>
            <h1 id="my-text">Oktay Kaypak</h1>
            <h1 id="my-text" class="bussines">UI & UX Developer</h1>
        </header>
    </section>
</template>

<script setup>
import { gsap } from 'gsap';
import SplitType from 'split-type'


onMounted(() => {
    const myText = new SplitType('#my-text')
    gsap.from('.char', {
        y: 100,
        stagger: 0.07,
        delay: 0.6,
        duration: 0.6,
    })
})
</script>

<style scoped lang="scss">
section {
    display: grid;
    place-content: center;
    height: 100vh;
}

h1 {
    font-size: 5rem;
    line-height: 1;
    text-transform: uppercase;
    font-family: 'Bebas Neue';
    clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);
    line-height: 5.9rem;
}

.bussines {
    font-size: 3rem;
    text-transform: uppercase;
    font-family: 'Bebas Neue';
    clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);
    line-height: 5.9rem;
}

.char {
    transform: translateY(115px);
    transition: transform .5s;
}
</style>