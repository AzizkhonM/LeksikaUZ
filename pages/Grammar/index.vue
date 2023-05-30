<script setup>

    import { grammar } from "../../constants/grammar"

</script>


<template>
    <div class="container mx-auto mt-[100px] pb-[160px]">
        <div class="px-[80px] py-[40px] bg-white">
            <h1 class="text-[24px] font-semibold text-center mb-[40px]">TABLE OF CONTENTS</h1>
            <ul v-for="i of grammar">
                <li class="w-full px-[32px] hover:bg-[#CBFDF4CC] duration-200 py-[24px] my-[10px] items-center rounded-full" style="display: grid; grid-template-columns: 5% 80% 5%; background-image: linear-gradient(to right, #D5DBF280 , #CBFDF4CC);">
                    <div class="px-[15px] py-[13px] bg-[#01756C] font-semibold text-[24px] rounded-full text-white flex justify-center items-center">{{ i.id }}</div>
                    <h1 class="ml-[30px] text-[18px]">{{ i.title }}</h1>
                    <nuxt-link :to="'/grammar/' + i.id" class="ml-[140px] hover:bg-[#01756c] hover:text-white duration-200 bg-white font-semibold rounded-full text-[#01756C] hover:cursor-pointer text-[24px] w-[50px] h-[50px] flex justify-center items-center"><i class='bx bx-plus' ></i></nuxt-link>
                </li>
            </ul>
        </div>
    </div>
</template>


<style lang="scss" scoped>

</style>