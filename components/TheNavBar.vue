<template>
    <div class="items-center">
        <nav class="transparent-navbar">
            <div class="navbar-content max-w-7xl  ">
                <!--Desktop menu-->
                <div class=" flex  ">
                    <div class="hidden sm:ml-6 sm:block">
                        <div class="flex space-x-4">
                            <a v-for="item in navigation" :key="item.name" :href="item.href"
                                class=" text-gray-500 rounded-full text-sm font-medium hover:text-gray-900"
                                aria-current="page">
                                {{ item.name }}
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </nav>
    </div>
</template>
<script setup>
const navigation = [
    { name: 'Home', href: '#', current: true },
    { name: 'History', href: '#', current: false },
    { name: 'Projects', href: '#', current: false },
]
</script>

<style>
.transparent-navbar {
    background-color: transparent;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 1000;
    transition: background-color 0.3s;
}

.transparent-navbar.scrolled {
    background-color: rgba(255, 255, 255, 0.8);
}

</style>
