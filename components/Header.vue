<script setup>

</script>


<template>
    <div class="bg-[#01756C] fixed w-screen">
        <div class="flex justify-between items-center py-[20px] container mx-auto">
            <nuxt-link to="/"><img src="../public/logo.svg" width="254" alt=""></nuxt-link>
            <ul class="flex w-[760px] justify-between items-center text-[18px] text-white">
                <li><nuxt-link to="/">ENG <i class='bx bx-transfer-alt'></i> UZB</nuxt-link></li>
                <li><nuxt-link to="/articles">Articles</nuxt-link></li>
                <li><nuxt-link to="/grammar">Grammar</nuxt-link></li>
                <li><nuxt-link to="/about">About us</nuxt-link></li>
            </ul>
        </div>
    </div>
</template>


<style scoped>

.router-link-exact-active{
  font-weight: 900
}

</style>