<template>
    <section class="md:flex items-center justify-between md:mx-5 mx-2">
        <div>
            <div class="flex items-center">
                <h2 class="text-xl font-bold">Senior Product Designer</h2>
            </div>
            <p class="text-sm text-gray-600">Purwokerto . Full Time</p>
        </div>
        <div class="mt-2 md:mt-0">
            <button type="button"
                class="focus:outline-none text-white bg-green-700 hover:bg-green-800 focus:ring-4 focus:ring-green-300 font-medium rounded-lg text-sm px-5 py-2.5 mr-2 mb-2 dark:bg-green-600 dark:hover:bg-green-700 dark:focus:ring-green-800">Share
                &amp; Promote</button>
            <button type="button"
                class="focus:outline-none text-white bg-green-700 hover:bg-green-800 focus:ring-4 focus:ring-green-300 font-medium rounded-lg text-sm px-5 py-2.5 mr-2 mb-2 dark:bg-green-600 dark:hover:bg-green-700 dark:focus:ring-green-800">Published</button>
        </div>
    </section>

    <section>
        <div class="mb-4 border-b border-gray-200 dark:border-gray-700">
            <ul class="flex flex-wrap -mb-px text-lg font-medium text-center" id="myTab" data-tabs-toggle="#myTabContent"
                role="tablist">
                <li class="mr-2" role="presentation">
                    <button class="inline-block p-4 border-b-2 rounded-t-lg" id="candidate-tab"
                        data-tabs-target="#candidate" type="button" role="tab" aria-controls="candidate"
                        aria-selected="false">Candidate</button>
                </li>
                <li class="mr-2" role="presentation">
                    <button
                        class="inline-block p-4 border-b-2 border-transparent rounded-t-lg hover:text-gray-600 hover:border-gray-300 dark:hover:text-gray-300"
                        id="job_details-tab" data-tabs-target="#job_details" type="button" role="tab"
                        aria-controls="job_details" aria-selected="false">Job details</button>
                </li>
                <li class="mr-2" role="presentation">
                    <button
                        class="inline-block p-4 border-b-2 border-transparent rounded-t-lg hover:text-gray-600 hover:border-gray-300 dark:hover:text-gray-300"
                        id="time_line-tab" data-tabs-target="#time_line" type="button" role="tab" aria-controls="time_line"
                        aria-selected="false">Time Line</button>
                </li>
                <li class="mr-2" role="presentation">
                    <button
                        class="inline-block p-4 border-b-2 border-transparent rounded-t-lg hover:text-gray-600 hover:border-gray-300 dark:hover:text-gray-300"
                        id="hiring_team-tab" data-tabs-target="#hiring_team" type="button" role="tab"
                        aria-controls="hiring_team" aria-selected="false">Hiring Team</button>
                </li>
                <li class="mr-2" role="presentation">
                    <button
                        class="inline-block p-4 border-b-2 border-transparent rounded-t-lg hover:text-gray-600 hover:border-gray-300 dark:hover:text-gray-300"
                        id="settings-tab" data-tabs-target="#settings" type="button" role="tab" aria-controls="settings"
                        aria-selected="false">Settings</button>
                </li>
            </ul>
        </div>
        <div id="myTabContent">
            <div class="hidden px-2 rounded-lg bg-gray-50 dark:bg-gray-800" id="candidate" role="tabpanel"
                aria-labelledby="candidate-tab">
                <IndexCandidate/>
            </div>
            <div class="hidden p-4 rounded-lg bg-gray-50 dark:bg-gray-800" id="job_details" role="tabpanel"
                aria-labelledby="job_details-tab">
                <p class="text-sm text-gray-500 dark:text-gray-400">job_details+This is some placeholder content the <strong
                        class="font-medium text-gray-800 dark:text-white">Dashboard tab's associated content</strong>.
                    Clicking another tab will toggle the visibility of this one for the next. The tab JavaScript swaps
                    classes to control the content visibility and styling.</p>
            </div>
            <div class="hidden p-4 rounded-lg bg-gray-50 dark:bg-gray-800" id="time_line" role="tabpanel"
                aria-labelledby="time_line-tab">
                <p class="text-sm text-gray-500 dark:text-gray-400">time_line + This is some placeholder content the <strong
                        class="font-medium text-gray-800 dark:text-white">Settings tab's associated content</strong>.
                    Clicking another tab will toggle the visibility of this one for the next. The tab JavaScript swaps
                    classes to control the content visibility and styling.</p>
            </div>
            <div class="hidden p-4 rounded-lg bg-gray-50 dark:bg-gray-800" id="hiring_team" role="tabpanel"
                aria-labelledby="hiring_team-tab">
                <p class="text-sm text-gray-500 dark:text-gray-400">hiring_team + This is some placeholder content the
                    <strong class="font-medium text-gray-800 dark:text-white">Contacts tab's associated content</strong>.
                    Clicking another tab will toggle the visibility of this one for the next. The tab JavaScript swaps
                    classes to control the content visibility and styling.
                </p>
            </div>
            <div class="hidden p-4 rounded-lg bg-gray-50 dark:bg-gray-800" id="settings" role="tabpanel"
                aria-labelledby="settings-tab">
                <p class="text-sm text-gray-500 dark:text-gray-400">settings + This is some placeholder content the <strong
                        class="font-medium text-gray-800 dark:text-white">Contacts tab's associated content</strong>.
                    Clicking another tab will toggle the visibility of this one for the next. The tab JavaScript swaps
                    classes to control the content visibility and styling.</p>
            </div>
        </div>
    </section>
</template>


<script setup>
import { onMounted } from 'vue'
import { initFlowbite } from 'flowbite'

// initialize components based on data attribute selectors
onMounted(() => {
    initFlowbite();
})


</script>