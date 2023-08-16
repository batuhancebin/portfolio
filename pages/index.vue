<template>
    <div>
        <div class="container">
            <section class="flex justify-center">
                <div>
                    <h1>
                        <span>Oktay</span>
                        <span>Kaypak</span>
                        <span>UI & UX Developer</span>
                    </h1>
                </div>
            </section>
            <section> </section>
        </div>
    </div>
</template>

<script setup>
// gsap animation
</script>

<style scoped lang="scss">
:root {
    --text-color: #111;
    --bg-color: #b9b3a9;
}


.container h1 {
    font-size: 5rem;
    line-height: 1;
    font-weight: 800;
    margin-bottom: 1rem;
    position: absolute;
    top: 15vw;
    left: 10vw;
    z-index: 4;
    overflow-wrap: break-word;
    hyphens: auto;

    @media (max-width: 768px) {
        font-size: 16vw;
    }

    span {
        display: block;
    }
}
</style>