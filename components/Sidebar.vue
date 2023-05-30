<script setup>

    import { latestArticles } from '../constants/latestArticles';
    import { tags } from "../constants/tags"

</script>


<template>
    
    <h1 class="font-semibold text-[24px] mb-[24px]">Latest articles</h1>
                <div class="py-[20px] px-[40px] bg-white mb-[40px] rounded-3xl">
                    <ul v-for="i of latestArticles" class="list-disc text-[16px] text-[#AAAAAA]">
                        <li :class="i.id != latestArticles.length ? 'pb-[15px]' : ''">{{ i.text }}</li>
                    </ul>
                </div>
                <h1 class="font-semibold text-[24px] mb-[24px]">Tags</h1>
                    <div v-for="i of tags">
                        <div class="p-[16px] text-[#aaaaaa] hover:drop-shadow-2xl duration-150 hover:cursor-pointer hover:bg-[#aaaaaa] hover:text-white bg-white mb-[16px] mr-[16px] w-auto inline-block rounded-full">{{i.text}}</div>
                    </div>
</template>


<style lang="scss" scoped>

</style>