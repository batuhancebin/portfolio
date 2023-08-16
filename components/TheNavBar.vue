<template>
    <div>
        <nav class="bg-gray-800">
            <div class="mx-auto max-w-7xl px-2 sm:px-6 lg:px-8">
                <div class="relative flex h-16 items-center justify-between">
                    <!--Desktop menu-->
                    <div class="flex flex-1 items-center justify-center sm:items-stretch sm:justify-start">

                        <div class="flex flex-shrink-0 items-center">
                            <img class="h-8 w-auto" src="https://tailwindui.com/img/logos/mark.svg?color=indigo&shade=500"
                                alt="Your Company">
                        </div>

                        <div class="hidden sm:ml-6 sm:block">
                            <div class="flex space-x-4">
                                <a v-for="item in navigation" :key="item.name" :href="item.href"
                                    class="bg-gray-800 text-white rounded-md px-3 py-2 text-sm font-medium hover:bg-white hover:text-gray-900"
                                    aria-current="page">
                                    {{ item.name }}
                                </a>
                            </div>
                        </div>

                    </div>

                </div>
            </div>

            <!-- Mobile menu, show/hide based on menu state. -->
            <div class="sm:hidden" id="mobile-menu">
                <div class="space-y-1 px-2 pb-3 pt-2">
                    <a v-for="item in navigation" :key="item.name" :href="item.href"
                        class="bg-gray-800 text-white block rounded-md px-3 py-2 text-base font-medium" aria-current="page">
                        {{ item.name }}
                    </a>>
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
    { name: 'Calendar', href: '#', current: false },
]
</script>
