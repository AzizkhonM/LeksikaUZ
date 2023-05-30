<script setup>

    import { articles } from '../../constants/articles';

</script>


<template>
    <div class="container m-auto mt-[100px] pb-[110px]">
        <div style="display: grid; grid-template-columns: 57% 40%;" class="gap-9 focus:drop-shadow-2xl mb-[20px]">
            <div class="">
                <div class="h-[64px] bg-white rounded-3xl flex px-[20px] mb-[20px]">
                    <img width="24" class="mr-[15px]" src="../../public/search.svg" alt="" /><input type="search"
                        class="text-[16px] w-[100%] rounded-3xl outline-none border-none" placeholder="Search articles here...">
                </div>
                <div v-for="i of articles">
                    <nuxt-link :to="'/articles/' + i.id" class="bg-white p-[20px] gap-7 rounded-3xl hover:shadow-2xl duration-200 mb-[20px]"
                        style="display: grid; grid-template-columns: 40% 55%;">
                        <img :src="i.img" class="w-[271px]" alt="">
                        <div class="grid grid-cols-1 ml-[-50px]">
                            <span class="text-[12px] text-[#8C8B8B] mb-[16px]"><i class='bx bxs-calendar text-[14px] mr-[10px]'></i>{{ i.time }}</span>
                            <h1 class="text-[24px] font-semibold mb-[16px]">{{ i.title }}</h1>
                            <p class="text-[16px] w-[370px]">{{ i.text }}</p>
                        </div>
                    </nuxt-link>
                </div>
            </div>
            <div class="">
                <Sidebar />
            </div>
        </div>

    </div>
</template>


<style lang="scss" scoped></style>