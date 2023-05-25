<template>
    <section class="md:mx-5 mx-2 mt-0 md:flex justify-between items-center">
        <div class="flex items-center">
            <p class="font-bold">Total Candidates: </p>
            <button class="bg-green-700 rounded-sm px-1 ml-2 text-white font-bold">22</button>
        </div>
        <div class="flex bg-gray-400 w-fit p-1 rounded-lg cursor-pointer mt-2 md:mt-0">
            <p class="px-3 py-1 font-bold bg-white rounded-md">Pipeline view</p>
            <p class="px-3 py-1 font-bold text-gray-800">Table view</p>
        </div>
    </section>
    <section class="grid grid-cols-12 gap-4 p-3">
        <div class="col-span-12 md:col-span-3 mb-5 p-3 border-t-4 rounded-md border-green-500 bg-white">

            <div class="flex justify-between items-center my-3">
                <h2 class="font-bold">New Applied</h2>
                <p class="font-bold">10</p>
            </div>

            <div v-for="c in candidateList">
                <IndexCandidateCard :details="c" />
            </div>

        </div>

        <div class="col-span-12 md:col-span-3 mb-5 p-3 border-t-4 rounded-md border-green-500 bg-white">

            <div class="flex justify-between items-center my-3">
                <h2 class="font-bold">New Applied</h2>
                <p class="font-bold">10</p>
            </div>

            <div v-for="c in candidateList">
                <IndexCandidateCard :details="c" />
            </div>

        </div>

        <div class="col-span-12 md:col-span-3 mb-5 p-3 border-t-4 rounded-md border-green-500 bg-white">

            <div class="flex justify-between items-center my-3">
                <h2 class="font-bold">New Applied</h2>
                <p class="font-bold">10</p>
            </div>

            <div v-for="c in candidateList">
                <IndexCandidateCard :details="c" />
            </div>

        </div>

        <div class="col-span-12 md:col-span-3 mb-5 p-3 border-t-4 rounded-md border-green-500 bg-white">

            <div class="flex justify-between items-center my-3">
                <h2 class="font-bold">New Applied</h2>
                <p class="font-bold">10</p>
            </div>

            <div v-for="c in candidateList">
                <IndexCandidateCard :details="c" />
            </div>

        </div>
    </section>
</template>

<script setup>
let candidateList = [{ "name": "Esther Gongela" }, { "name": "Lubrica Fannandes" }, { "name": "Ariyana Grozza" }];
</script>