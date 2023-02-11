<template>
    <nav class="bg-white border-gray-200 px-2 sm:px-4 py-2.5 rounded dark:bg-gray-900">
        <div class="container flex flex-wrap items-center mx-auto">
            <a href="/" class="flex items-center">
                <img src="@/assets/imgs/cover.png" class="h-6 mr-3 sm:h-9 rounded" alt="The Stuff Cover Logo" />
            </a>
            <ul
                class="flex flex-col p-4 mt-4 border border-gray-100 rounded-lg bg-gray-50 md:flex-row md:space-x-8 md:mt-0 md:text-sm md:font-medium md:border-0 md:bg-white dark:bg-gray-800 md:dark:bg-gray-900 dark:border-gray-700">
                <li v-for="navRoutes in navigationRoutes" :to="navRoutes.link">
                    <a :href="navRoutes.link"
                        class="block py-2 pl-3 pr-4 text-white bg-blue-700 rounded md:bg-transparent md:text-blue-700 md:p-0 dark:text-white"
                        aria-current="page">{{ navRoutes.name }}</a>
                </li>
            </ul>
        </div>
    </nav>
</template>

<script>
export default {
    props: {
        navigationRoutes: Array,
    },
    data() {
        return {
            isActive: false,
            showNavbar: true
        }
    }
}
</script>