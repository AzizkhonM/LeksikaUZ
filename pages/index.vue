<script setup>

const search = ref();
let result = ref([]);
const partOfSpeech = ref("");
const audio = ref("")
const definition = ref("")
const get = async () => {
    definition.value = ""
    result.value = ""
    audio.value = ""
    partOfSpeech.value = "";
    const { data } = await useFetch(
        `https://api.dictionaryapi.dev/api/v2/entries/en/${search.value.toLowerCase()}`
    );
    result.value = data.value;
    console.log(result.value);
    console.log(result.value[0].phonetics[1].text);
    if (result.value != null) {
        for(let i of result.value[0].meanings[0].definitions){
            if(i.definition != ""){
                console.log(i.definition);
                definition.value += i.definition + "\n"
            }
        }
        for (let i of result.value[0].meanings) {
            partOfSpeech.value += `${i.partOfSpeech}, `;
        }
        for (let i of result.value[0].phonetics) {
            console.log(i);
            if (i.audio != "") {
                audio.value = i.audio
                break
            }
        }
        console.log(audio.value.length);
        partOfSpeech.value = partOfSpeech.value.slice(0, partOfSpeech.value.length - 2);
    }
};

const playAudio = async () => {
    var audio = document.getElementById("audio");
    await audio.play();
}
</script>

<template>
    <div class="flex justify-center mb-10 mt-[100px]">
        <form @submit.prevent="get" class="w-[847px] flex justify-between p-[5px] rounded-full items-center bg-white">
            <div class="text-[16px] py-[20px] px-[36px] rounded-full bg-[#01756C] text-white">
                ENG <i class="bx bx-transfer-alt"></i> UZB
            </div>
            <img src="../public/search.svg" alt="" />
            <input v-model="search" class="w-[75%] h-[100%] rounded-full outline-none border-none text-[16px]"
                placeholder="Search words here..." type="search" />
        </form>
    </div>
    <!-- {{ result }} -->
    <div class="m-auto w-[600px] text-center">
        <h1 v-if="!result?.length" class="z-10 text-[24px]">
            Search any words, we find this word's definition, translation and etc.
        </h1>
        <div v-else>
            <h2 v-if="result == null">
                UXla
            </h2>
            <div v-else class="flex justify-center items-center">
                <div class="bg-white h-auto mb-[250px] w-[847px] py-[30px] px-[32px]">
                    <!-- {{ result }} -->
                    <div class="text-[32px] text-left font-extrabold mb-[25px]">
                        {{ result[0].word }}
                    </div>
                    <div class="text-left italic text-[#8C8B8B] mb-[18px]">{{ partOfSpeech }}</div>
                    <div class="mb-[18px] text-left">
                        <i v-if="audio.length != 0"
                            class="bx bx-volume-full text-[18px] text-black mr-[15px] cursor-pointer"
                            @click="playAudio"></i>
                        <audio id="audio" :src="audio"></audio>
                        <span v-if="result[0].phonetics[1].text" class="text-[#8C8B8B] text-[18px]">
                            {{ result[0].phonetics[1].text }}</span>
                    </div>
                    <div class="text-left">
                        <h1>{{ definition }}</h1>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped></style>
