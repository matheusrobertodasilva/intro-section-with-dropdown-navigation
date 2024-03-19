<style>
   
</style>

<template>
    <header class="m-5 flex justify-between items-center lg:justify-between">
        <img src="../assets/images/logo.svg" alt="Logo">
        <button @click="mudarButton" class="z-50 lg:hidden"><img :src="iconeMenu" alt=""></button>
        <nav class="absolute top-0 right-0 pt-20 px-5 w-[65vw] h-screen 
        lg:static lg:opacity-100 lg:pointer-events-auto lg:flex lg:justify-between lg:items-center lg:h-auto lg:p-0 lg:w-full"
        :class="[menuAberto ? 'translate-x-0 duration-500 ease-in-out ':'-translate-x-0 opacity-0 duration-500 ease-in-out pointer-events-none']"
        >
            <ul class="lg:flex items-center">
                <li class="my-3 lg:ml-10">
                    <a href="#"class="flex items-center lg:hover:text-Almost-Black " @click="[features = !features]" >Features 
                        <img alt="" class="ml-3"
                        :src="[features ? 'src/assets/images/icon-arrow-up.svg':'/src/assets/images/icon-arrow-down.svg']"
                        >
                    </a>
                    <ul class="ml-5 my-5 lg:absolute lg:top-10 lg:left-[-35px] lg:bg-Almost-White lg:px-8 lg:rounded-xl lg:shadow-2xl"
                    :class="[features ? 'duration-500 block':'duration-500 hidden']"
                    >
                        <li class="my-3">
                            <a href="" class="flex items-center">
                                <img src="/src/assets/images/icon-todo.svg" alt="icone" class="mr-3">Todo list
                            </a>
                        </li>
                        <li class="my-3">
                            <a href="" class="flex items-center">
                                <img src="/src/assets/images/icon-calendar.svg" alt="icone" class="mr-3">
                                Calendar
                            </a>
                        </li>
                        <li class="my-3">
                            <a href="" class="flex items-center">
                                <img src="/src/assets/images/icon-reminders.svg" alt="icone" class="mr-3">
                                Reminders
                            </a>
                        </li>
                        <li class="my-3">
                            <a href="" class="flex items-center">
                                <img src="/src/assets/images/icon-planning.svg" alt="icone" class="mr-3">
                                Planning
                            </a>
                        </li>
                    </ul>
                </li>
                <li class="my-3 lg:ml-10 ">
                    <a href="#"class="flex items-center lg:hover:text-Almost-Black" @click="[company = !company]" >Company 
                        <img alt="" class="ml-3" 
                        :src="[company ? 'src/assets/images/icon-arrow-up.svg':'/src/assets/images/icon-arrow-down.svg']"
                        >
                    </a>
                    <ul class="ml-5 my-5 
                    lg:absolute lg:top-10 lg:left-40 lg:bg-Almost-White  lg:px-5 lg:py-2 lg:rounded-xl lg:shadow-2xl"
                    :class="[company ? 'duration-500 block':'duration-500 hidden']"
                    >
                        <li class="my-3">History</li>
                        <li class="my-3">Our Team</li>
                        <li class="my-3">Blog</li>
                    </ul>
                </li>
                <li class="my-3 lg:ml-10 lg:hover:text-Almost-Black"><a href="#">Careers</a></li>
                <li class="my-3 lg:ml-10 lg:hover:text-Almost-Black"><a href="#">About</a></li>
            </ul>
            <div class="flex flex-col lg:flex-row">
                <button class="my-1 lg:mr-5 lg:hover:text-Almost-Black">Login</button>
                <button class="border-2 border-Medium-Gray rounded-xl p-[5px] lg:px-[20px] my-2 lg:hover:text-Almost-Black lg:hover:border-Almost-Black">Register</button>
            </div>
        </nav>
    </header>
</template>

<script>
    import { defineComponent } from 'vue';
    export default defineComponent ({
        data(){
            return{
                iconeMenu: "src/assets/images/icon-menu.svg",
                menuAberto:false,
                features: false,
                company: false
            }
        },
        methods:{
            mudarButton(){
                if(this.iconeMenu == "src/assets/images/icon-menu.svg"){
                    this.iconeMenu = "src/assets/images/icon-close-menu.svg"
                    this.menuAberto = true
                } else{
                    this.iconeMenu = "src/assets/images/icon-menu.svg"
                    this.menuAberto = false
                }
            }
        }
    })
</script>