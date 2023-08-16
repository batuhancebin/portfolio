<template>
    <div>
        <section class="flex justify-center">
            <div class="container">
                <h1 class="split">Oktay</h1>
                <h1 class="split2">Kaypak</h1>
                <h1 class="split work">UI & UX Developer</h1>
            </div>
        </section>
        <section style="height: 2000px;">

        </section>
    </div>
</template>

<script setup>
import { gsap } from 'gsap';
import { Observer } from 'gsap/Observer';
import { Draggable } from 'gsap/Draggable';

gsap.registerPlugin(Observer);

onMounted(() => {
    function rotate(value) {
        gsap.to('.split', {
            rotate: value + '_short',
            ease: 'back.out',
            duration: 0.5,
            overwrite: true,
            transformOrigin: 'center center',
        }),
            gsap.to('.split2', {
                rotate: -value + '_short',
                ease: 'back.out',
                duration: 0.5,
                overwrite: true,
                transformOrigin: 'center center',
            })
    }
    Observer.create({
        target: window,
        types: "wheel.touch.scroll.pointer",
        onUp: () => { rotate('0') },
        onDown: () => { rotate('180') },
        onChange: (self) => {
            if (self.direction === 1) {
                rotate('180')
            } else {
                rotate('0')
            }
        }
    })

})


</script>

<style scoped lang="scss">
:root {
    --text-color: #111;
    --bg-color: #b9b3a9;
}


.container {
    font-size: 5rem;
    line-height: 1;
    font-weight: 800;
    margin-bottom: 1rem;
    position: absolute;
    top: 15vw;
    left: 10vw;
    z-index: 4;

    @media (max-width: 768px) {
        font-size: 16vw;
    }


}
</style>