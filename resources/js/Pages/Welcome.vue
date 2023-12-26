<script setup>
import { Head, Link } from '@inertiajs/vue3';
import { SearchIcon, MenuFoldLineRightIcon } from '@/Components/Icons/outline.jsx';
import Button from '@/Components/Button.vue';
import { ref } from 'vue';

const navShow = ref(false);

defineProps({
    canLogin: Boolean,
    canRegister: Boolean,
    laravelVersion: String,
    phpVersion: String,
})
</script>

<template>
    <Head title="Landing Page" />

    <!-- Navbar -->
    <nav class="container mx-auto flex items-center justify-between py-5 px-4 md:px-0 lg:px-0">
        <h1 class="text-2xl">SportsBlogs</h1>
        <div class="hidden md:flex md:flex-row items-center justify-center gap-9">
            <Link href="#">NBA</Link>
            <Link href="#">NFL</Link>
            <Link href="#">NHL</Link>
            <Link href="#">MLD</Link>
            <Link href="#">SOCCER</Link>
        </div>
        <button @click="navShow = !navShow" class="md:hidden">
            <MenuFoldLineRightIcon class="w-6 h-6" />
        </button>
        <div class="hidden md:flex lg:flex items-center gap-4 justify-end">
            <SearchIcon class="w-6 h-6" />
            <Button href="/login" type="button">Sign In</Button>
        </div>
    </nav>
    <Transition>
        <div v-if="navShow" class="relative z-10">
            <div class="relative w-screen h-screen top-0 bg-white">
                <div class="flex flex-col mt-10 items-center justify-center gap-6 text-xl mx-auto w-11/12">
                    <Link href="#" class="w-full text-center">NBA</Link>
                    <Link href="#" class="w-full text-center">NFL</Link>
                    <Link href="#" class="w-full text-center">NHL</Link>
                    <Link href="#" class="w-full text-center">MLD</Link>
                    <Link href="#" class="w-full text-center">SOCCER</Link>
                    <Link class="bg-purple-500 w-full text-center text-white py-2 rounded-lg">Sign In</Link>
                </div>
            </div>
        </div>
    </Transition>

    <!-- End Nav -->

    <main>
        <!-- Hero -->
        <div
            class="container flex items-center md:rounded-lg justify-center mx-auto w-full h-[23rem] md:h-[19rem] bg-[#16243E]">
            <Link class="text-white border border-3 border-white px-8 py-2 rounded-xl hover:bg-white hover:text-black">
            Subscribe
            </Link>
        </div>
        <!-- End Hero -->

        <!-- Blogs -->
        <div class="container mx-auto py-5 px-4 md:px-0 lg:px-0">
            <div class="flex flex-col gap-14 justify-between md:flex-row">
                <!-- Card -->
                <div class="flex flex-col w-full h-full md:w-1/2">
                    <img class="rounded-xl" src="../Components/assets/images/thumbnail.png" alt="">
                    <h1 class="mt-4 text-2xl font-semibold">Melvin Gordon is making the right decision walking away from the
                        Chargers
                    </h1>
                    <div class="flex text-gray-500 gap-2">
                        <p>By Gabie Sheber</p>
                        <p>-</p>
                        <p>Mar 28, 2020</p>
                    </div>
                </div>
                <!-- End Card -->

                <div class="flex flex-col w-full h-full md:w-1/2 gap-12">
                    <div class="flex w-full h-full gap-2">
                        <img class="w-1/3 rounded-xl" src="../Components/assets/images/thumbnail2.png" alt="">
                        <div class="flex flex-col">
                            <h1 class="text-2xl max-w-[75%] font-semibold">Titans Post Elite PFF Tackling in 2019</h1>
                            <div class="flex text-gray-500 gap-2">
                                <p>By Gabie Sheber</p>
                                <p>-</p>
                                <p>Mar 28, 2020</p>
                            </div>
                        </div>
                    </div>
                    <div class="flex w-full h-full gap-2">
                        <img class="w-1/3 rounded-xl" src="../Components/assets/images/thumbnail2.png" alt="">
                        <div class="flex flex-col">
                            <h1 class="text-2xl max-w-[75%] font-semibold">Titans Post Elite PFF Tackling in 2019</h1>
                            <div class="flex text-gray-500 gap-2">
                                <p>By Gabie Sheber</p>
                                <p>-</p>
                                <p>Mar 28, 2020</p>
                            </div>
                        </div>
                    </div>
                    <div class="flex w-full h-full gap-2">
                        <img class="w-1/3 rounded-xl" src="../Components/assets/images/thumbnail2.png" alt="">
                        <div class="flex flex-col">
                            <h1 class="text-2xl max-w-[75%] font-semibold">Titans Post Elite PFF Tackling in 2019</h1>
                            <div class="flex text-gray-500 gap-2">
                                <p>By Gabie Sheber</p>
                                <p>-</p>
                                <p>Mar 28, 2020</p>
                            </div>
                        </div>
                    </div>

                </div>
            </div>
        </div>
        <!-- EndBlogs -->
    </main>

    <footer>
        <div class="w-full bg-slate-300 p-8 rounded-lg">
            <div class="flex flex-col gap-24 pt-24">
                <div class="flex items-center justify-center">
                    <div class="relative flex items-center w-1/3">
                        <input type="text"
                            class="-z-2 w-full border border-solid focus:outline-none focus:ring-0 focus:border-purple-500 border-transparent rounded-3xl"
                            placeholder="Your@gmail.com">
                        <Button class="rounded-3xl z-2 absolute right-0">Send</Button>
                    </div>
                </div>

                <div class="container mx-auto flex items-center justify-between">
                    <div class="flex justify-center items-center gap-9 text-white">
                        <Link href="#">ABOUT</Link>
                        <Link href="#">CONTACT US</Link>
                        <Link href="#">HELP</Link>
                        <Link href="#">STORE</Link>
                    </div>
                    <div class="flex">
                        <svg width="108" class="fill-white" height="26" viewBox="0 0 108 26" fill="none"
                            xmlns="http://www.w3.org/2000/svg">
                            <path
                                d="M101.5 0H88.5C84.9253 0 82 2.92532 82 6.5V19.5006C82 23.0744 84.9253 26.0006 88.5 26.0006H101.5C105.075 26.0006 108 23.0744 108 19.5006V6.5C108 2.92532 105.075 0 101.5 0ZM105.833 19.5006C105.833 21.8894 103.89 23.8339 101.5 23.8339H88.5C86.1109 23.8339 84.1668 21.8894 84.1668 19.5006V6.5C84.1668 4.11062 86.1109 2.16677 88.5 2.16677H101.5C103.89 2.16677 105.833 4.11062 105.833 6.5V19.5006Z" />
                            <path
                                d="M101.215 15.4449H99.0091V24.3754H95.741C95.741 24.3754 95.741 19.4957 95.741 15.4449H94.1875V12.2885H95.741V10.2469C95.741 8.78475 96.3526 6.5 99.0391 6.5L101.461 6.51055V9.57446C101.461 9.57446 99.9893 9.57446 99.7031 9.57446C99.417 9.57446 99.0102 9.73699 99.0102 10.4343V12.2891H101.5L101.215 15.4449Z" />
                            <path
                                d="M60.5 0H47.5C43.9253 0 41 2.92532 41 6.5V19.5006C41 23.0744 43.9253 26.0006 47.5 26.0006H60.5C64.0747 26.0006 67 23.0744 67 19.5006V6.5C67 2.92532 64.0747 0 60.5 0ZM64.8332 19.5006C64.8332 21.8894 62.8901 23.8339 60.5 23.8339H47.5C45.1109 23.8339 43.1668 21.8894 43.1668 19.5006V6.5C43.1668 4.11062 45.1109 2.16677 47.5 2.16677H60.5C62.8901 2.16677 64.8332 4.11062 64.8332 6.5V19.5006Z" />
                            <path
                                d="M61.052 8.90393C60.9949 8.92137 60.9374 8.93793 60.8795 8.9536C60.6828 9.0068 60.5396 8.76076 60.6799 8.61069C60.8272 8.45323 60.9569 8.27897 61.066 8.09118C61.1682 7.91521 60.9882 7.71049 60.8056 7.79567C60.4269 7.97221 60.0259 8.10837 59.6079 8.19955C59.5403 8.21427 59.4706 8.19089 59.4212 8.1416C57.5025 6.22577 54.1718 7.87585 54.5743 10.5864C54.5939 10.7184 54.4847 10.833 54.3541 10.8222C52.1913 10.6422 50.2686 9.61458 48.917 8.07084C48.8189 7.95881 48.6396 7.98611 48.5791 8.12297C48.1231 9.15522 48.3165 10.3699 49.0715 11.2085C49.212 11.3646 49.0637 11.611 48.8646 11.5499C48.671 11.4905 48.486 11.4112 48.3125 11.3146V11.351C48.3125 12.4372 48.9149 13.3833 49.8029 13.8711C49.9829 13.97 49.9522 14.2816 49.6481 14.2591C49.4936 14.2478 49.381 14.4097 49.4475 14.5522C49.8254 15.3628 50.5699 15.9676 51.467 16.1516C51.6483 16.1887 51.6921 16.4316 51.5354 16.5319C50.6386 17.1064 49.6216 17.408 48.5951 17.4365C48.3824 17.4423 48.3186 17.7346 48.5096 17.8303C49.6029 18.3779 50.835 18.6878 52.1392 18.6878C57.4043 18.6878 60.2821 14.3135 60.2821 10.5193C60.2821 10.4317 60.2813 10.344 60.2788 10.2568C60.2769 10.1883 60.3078 10.124 60.3619 10.0833C60.6899 9.83642 60.9915 9.55386 61.2605 9.24261C61.3958 9.08603 61.2481 8.8441 61.052 8.90393Z" />
                            <path
                                d="M19.5 0H6.5C2.92532 0 0 2.92532 0 6.5V19.5006C0 23.0744 2.92532 26.0006 6.5 26.0006H19.5C23.0747 26.0006 26 23.0744 26 19.5006V6.5C26 2.92532 23.0747 0 19.5 0ZM23.8332 19.5006C23.8332 21.8894 21.8901 23.8339 19.5 23.8339H6.5C4.11093 23.8339 2.16677 21.8894 2.16677 19.5006V6.5C2.16677 4.11062 4.11093 2.16677 6.5 2.16677H19.5C21.8901 2.16677 23.8332 4.11062 23.8332 6.5V19.5006Z" />
                            <path
                                d="M13 6.5C9.40938 6.5 6.5 9.4097 6.5 13C6.5 16.589 9.40938 19.5006 13 19.5006C16.5896 19.5006 19.5 16.589 19.5 13C19.5 9.4097 16.5896 6.5 13 6.5ZM13 17.3339C10.607 17.3339 8.66677 15.3936 8.66677 13C8.66677 10.6064 10.607 8.66677 13 8.66677C15.393 8.66677 17.3332 10.6064 17.3332 13C17.3332 15.3936 15.393 17.3339 13 17.3339Z" />
                        </svg>
                    </div>
                    <div class="flex text-white">
                        <p>
                            Designed by
                            <a target="_blank" href="https://www.figma.com/@uchiha5555"
                                class="hover:text-black hover:underline">
                                Uchiha5555</a> &
                            Developed By
                            <a target="_blank" href="https://github.com/maulanahusains"
                                class="hover:text-black hover:underline">
                                Maulana</a>
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<style scoped>
.v-enter-active,
.v-leave-active {
    transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
    opacity: 0;
}
</style>