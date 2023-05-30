<script setup>

    const Akbar = ref(false)
    const Asqar = ref(false)

    const AkbarModal = () => Akbar.value = !Akbar.value
    const AsqarModal = () => Asqar.value = !Asqar.value

</script>


<template>


    <!-- Main modal -->
<div id="defaultModal" tabindex="-1" aria-hidden="true" :class="Akbar ? 'bg-[rgba(0,0,0,0.4)] overflow-y-auto flex overflow-x-hidden fixed top-0 right-0 left-0 z-50 justify-center items-center w-full md:inset-0 h-modal md:h-full' : 'hidden'">
    <div class="relative p-4 w-full max-w-2xl h-full md:h-auto">
        <!-- Modal content -->
        <div class="relative p-4 bg-white rounded-lg dark:bg-gray-800 sm:p-5">
            <!-- Modal header -->
            <div class="flex items-center justify-between  px-5 py-3 mb-4 rounded-2xl sm:mb-5">
                <h3 class="text-[24px] font-semibold text-black dark:text-white">
                    Akbar Kholmuradov
                </h3>
                <button @click="AkbarModal" type="button" class="text-black bg-transparent hover:bg-black duration-300 hover:text-white rounded-lg text-sm p-1.5 ml-auto inline-flex items-center dark:hover:bg-gray-600 dark:hover:text-white" data-modal-toggle="defaultModal">
                    <svg aria-hidden="true" class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
                    <span class="sr-only">Close modal</span>
                </button>
            </div>
            <div class="p-4 indent-[30px]">
                <h1 class="mb-[20px]">Having graduated the International Economic Relations department of the University of World Economy and Diplomacy in 2001, Akbar dedicated his later years to translation and localization. When working as a translator in various huge projects, he faced the difficulty in finding reliable sources that can be used in translation to/from Uzbek language, and as a result some books for English learners and translators were published</h1>
                <h1 class="mb-[20px]"><b>English-Uzbek-English dictionary</b> (<span class="text-[#01756C] hover:underline hover:cursor-pointer">book</span>, <span class="text-[#01756C] hover:underline hover:cursor-pointer">app</span>)</h1>
                <h1 class="mb-[20px]"><b>English Grammar for Uzbek Learners</b> (<span class="text-[#01756C] hover:underline hover:cursor-pointer">book</span>, <span class="text-[#01756C] hover:underline hover:cursor-pointer">app</span>)</h1>
            </div>
        </div>
    </div>
</div>




<div id="defaultModal" tabindex="-1" aria-hidden="true" :class="Asqar ? 'bg-[rgba(0,0,0,0.4)] overflow-y-auto flex overflow-x-hidden fixed top-0 right-0 left-0 z-50 justify-center items-center w-full md:inset-0 h-modal md:h-full' : 'hidden'">
    <div class="relative p-4 w-full max-w-2xl h-full md:h-auto">
        <!-- Modal content -->
        <div class="relative p-4 bg-white rounded-lg dark:bg-gray-800 sm:p-5">
            <!-- Modal header -->
            <div class="flex items-center justify-between  px-5 py-3 mb-4 rounded-2xl sm:mb-5">
                <h3 class="text-[24px] font-semibold text-black dark:text-white">
                    Asqar Arslonov
                </h3>
                <button @click="AsqarModal" type="button" class="text-black bg-transparent hover:bg-black duration-300 hover:text-white rounded-lg text-sm p-1.5 ml-auto inline-flex items-center dark:hover:bg-gray-600 dark:hover:text-white" data-modal-toggle="defaultModal">
                    <svg aria-hidden="true" class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
                    <span class="sr-only">Close modal</span>
                </button>
            </div>
            <div class="p-4 indent-[30px]">
                <h1 class="mb-[20px]">Having started his IT-education at the age of 12, Asqarjon has reached the level of full-stack developer just 2 years later. Taking several online courses (Technical Support Fundamentals, Computer Networking) was followed by successful completion of Front-End Development and Back-End Development courses at the Open Web Academy education center in Qarshi city. Being an eighth-grader, he is fully responsible for the technical support of Leksika.uz</h1>
            </div>
        </div>
    </div>
</div>


    <div class="container m-auto mt-[100px] pb-[110px]">
        <div class="border-b-2 pb-[80px]">
            <h1 class="w-[846px] text-center text-[18px] m-auto">Remember the days when you couldn’t find the proper
                translation of an English word to the Uzbek language? I also know those feelings when you run against the
                lack of general use dictionaries - not to mention the specialized ones, a total absence of online resources
                in Uzbek, a pre-requisite of knowing the Russian language in order to apply indirect translation (EN RU UZ
                and vice versa).</h1>
        </div>
        <div class="py-[61px] border-b-2">
            <div style="display: grid; grid-template-columns: 40% 60%;" class="mb-[61px]">
                <div>
                    <h1 class="text-[#01756C] text-[24px] font-semibold">Book edition</h1>
                </div>
                <div>
                    <p class="text-[16px] mb-2">To reverse the situation, it was decided to compile a large
                        English-Uzbek-English
                        dictionary and the work
                        started back in 2003. 2 years later, the <span class="text-[#01756C]">first edition</span> of the
                        bilingual dictionary was published in
                        G’afur G’ulom publishing house; it is still <span class="text-[#01756C]">available</span> for sale
                        online. Much attention was directed
                        to
                        the Uzbek-English part; even now, it is the most comprehensive and complete UZ-EN dictionary.</p>
                    <p>A <span class="text-[#01756C]">mobile app</span> for Android devices was launched based on the
                        dictionary with ma jor update of the lexical database.</p>
                </div>
            </div>
            <div style="display: grid; grid-template-columns: 40% 60%;" class="mb-[61px]">
                <div>
                    <h1 class="text-[#01756C] text-[24px] font-semibold">Website dictionary</h1>
                </div>
                <div>
                    <p class="text-[16px] mb-2">However, we still desperately needed a high-quality online dictionary for
                        English-Uzbek language pair that could cover both everyday and area-specific vocabulary. In
                        September 2022, on the date of 31th anniversary of Independence of Uzbekistan, Leksika.uz was
                        successfully launched.</p>
                    <p>Leksika.uz has mainly been designed to give English learners of any level the help they need to read,
                        speak and write English more effectively. It is also intended to assist translators and localizers
                        by providing useful tips and rules of thumb; these can be found in Localization section.</p>
                </div>
            </div>
            <div style="display: grid; grid-template-columns: 40% 60%;">
                <div>
                    <h1 class="text-[#01756C] text-[24px] font-semibold">Prospects</h1>
                </div>
                <div>
                    <ul class="list-disc ml-5 text-[16px]">
                        <li>Russian-Uzbek-Russian dictionary section with largest database on the web;</li>
                        <li>content for easier learning of English, including grammar, writing tips, learning new words;
                        </li>
                        <li>useful tips and motivational articles for freelancers;</li>
                        <li>articles for localizers to Uzbek language, including intricacies of Uzbek grammar;</li>
                        <li>and much more.</li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="py-[61px]">
            <div style="display: grid; grid-template-columns: 40% 60%;">
                <div>
                    <h1 class="text-[#01756C] text-[24px] font-semibold">Our team</h1>
                </div>
                <div class="flex justify-center items-center gap-[100px]">
                    <div @click="AkbarModal" class="w-[50%] bg-white pb-[20px] rounded-2xl hover:drop-shadow-2xl duration-200 hover:cursor-pointer">
                        <img src="../../public/team1.png" class="mb-[20px]" alt="">
                        <h1 class="text-center text-[24px] font-semibold">Akbar Kholmuradov</h1>
                        <div class="flex justify-center">
                            <img src="../../public/line.png" class="my-[10px]" alt="">
                        </div>
                        <h1 class="text-[#8C8B8B] text-center text-[18px]">Founder and content manager</h1>
                    </div>
                    <div @click="AsqarModal" class="w-[50%] bg-white pb-[20px] rounded-2xl hover:drop-shadow-2xl duration-200  hover:cursor-pointer">
                        <img src="../../public/team2.png" class="mb-[20px]" alt="">
                        <h1 class="text-center text-[24px] font-semibold">Asqar Arslonov</h1>
                        <div class="flex justify-center">
                            <img src="../../public/line.png" class="my-[10px]" alt="">
                        </div>
                        <h1 class="text-[#8C8B8B] text-center text-[18px]">Full-Stack (MERN) Developer</h1>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>


<style lang="scss" scoped></style>