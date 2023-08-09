<template>
    <div class="layout-home w-[100%]
     flex-col flex ">
        <!-- submenu -->
        <div class="flex sub-menu sm:flex-wrap 
            bg-[#fff] shadow-md">
            <!-- menu -->
            <div class="flex container mx-auto items-center">
                <div class="w-[30%] items-center flex gap-4 justify-start items-start">
                    <nuxt-link to="/">
                        <font-awesome-icon class="icon-font" icon="fa-brands fa-facebook" />
                    </nuxt-link>
                    <nuxt-link to="/">
                        <font-awesome-icon class="icon-font" icon="fa-brands fa-twitter" />
                    </nuxt-link>
                    <nuxt-link to="/">
                        <font-awesome-icon class="icon-font" icon="fa-brands fa-instagram" />
                    </nuxt-link>
                    <nuxt-link to="/">
                        <font-awesome-icon class="icon-font" icon="fa-brands  fa-youtube" />
                    </nuxt-link>
                </div>
                <div class="w-[70%] flex  justify-between items-center">
                <!-- location -->
                    <div class="flex gap-1 w-[25%]">
                        <font-awesome-icon class="icon-font" icon="fa-brands  fa-youtube" />
                        <p class="f14-400">Lorem Ipsum is simply</p>
                    </div>
                <!-- email -->
                    <div class="flex gap-1 w-[25%]">
                        <font-awesome-icon class="icon-font" icon="fa-brands  fa-youtube" />
                        <p class="f14-400">demo@gmail.com</p>
                    </div>
                    <!-- contact us -->
                    <div class="flex gap-1 w-[35%] justify-center items-center bg-[#10c695] p-5">
                        <font-awesome-icon class="icon-font" icon="fa-brands  fa-youtube" />
                        <p class="f22-700 text-white">
                            
                            Call : +01 1234567890
                  
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <!-- menu and slider -->
        <div class="flex flex-col slider-header relative w-[100%]">
            <img src="../assets/img/slider.jpg" alt="">
            <!-- menu -->
            <div class="flex menu container mx-auto absolute">
                menu
            </div>
            <div class="flex container mx-auto">
                slider
            </div>
        </div>
        <!-- slot show data home page -->
        <div class="flex flex-col body-home w-[100]">
            <div class="flex container mx-auto">
                <slot />
            </div>
        </div>
        <!-- footer -->
        <div class="footer flex">
            <div class="flex container mx-auto">
                footer
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">

</script>

<style lang="scss" scoped>
    .slider-header{
        position: relative;
        height: 100vh;
        img{
            width: 100%;
            height: 100vh;
            object-fit: cover;
        }
        .menu{
           left: 32px;
        }
        ::after{
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 97.5%;
            background: linear-gradient(125deg, rgba(31, 65, 114, 0.85), rgba(31, 65, 114, 0.75), rgba(31, 65, 114, 0.05));
        }
    }
    .icon-font{
        color: #10c695;
        font-size: 27px;
    }
</style>