<script setup>
    import Header from './Header.vue';
</script>

<template>
    <Header/>
    <main>
        <section>
            <div class="lg:flex lg:flex-row-reverse lg:m-20 ">
                <img src="/src/assets/images/image-hero-mobile.png" alt="" class="lg:hidden">
                <img src="/src/assets/images/image-hero-desktop.png" alt="" class="w-[35vw] hidden lg:block">
                <div class="text-center m-5 
                lg:text-start lg:flex lg:flex-col lg:justify-end lg:items-start lg:mr-20 lg:my-0">
                    <h1 class="text-Almost-Black font-bold text-[35px] mt-5
                    lg:mt-0 lg:text-[78px] lg:pr-[160px] lg:leading-[80px]">Make remote work </h1>
                    <p class="my-3 text-[16px] lg:text-[18px] lg:pr-[200px] lg:my-[40px]">Get your team in sync, no matter your location. Streamline processes, create team rituals, and watch productivity soar.</p>
                    <button class="bg-Almost-Black rounded-xl py-2 px-5 lg:py-[15px] lg:px-[25px] my-5 text-Almost-White font-bold">Learn more</button>
                    <div class="flex justify-around items-center my-4">
                        <img class="w-[18vw] lg:w-[8vw] m-2 lg:m-0 lg:mx-5 lg:mt-10" src="/src/assets/images/client-databiz.svg" alt="">
                        <img class="w-[18vw] lg:w-[8vw] m-2 lg:m-0 lg:mx-5 lg:mt-10" src="/src/assets/images/client-audiophile.svg" alt="">
                        <img class="w-[18vw] lg:w-[8vw] m-2 lg:m-0 lg:mx-5 lg:mt-10" src="/src/assets/images/client-meet.svg" alt="">
                        <img class="w-[18vw] lg:w-[8vw] m-2 lg:m-0 lg:mx-5 lg:mt-10" src="/src/assets/images/client-maker.svg" alt="">
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>