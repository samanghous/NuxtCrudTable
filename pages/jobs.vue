<template>
    <div class="mb-4 border-b border-gray-200 dark:border-gray-700">
        <ul class="flex flex-wrap -mb-px text-sm font-medium text-center" id="myTab" data-tabs-toggle="#myTabContent"
            role="tablist">
            <li class="mr-2" role="presentation">
                <button class="inline-block p-4 border-b-2 rounded-t-lg" id="active_jobs-tab" data-tabs-target="#active_jobs"
                    type="button" role="tab" aria-controls="active_jobs" aria-selected="false">Active Jobs</button>
            </li>
            <li class="mr-2" role="presentation">
                <button
                    class="inline-block p-4 border-b-2 border-transparent rounded-t-lg hover:text-gray-600 hover:border-gray-300 dark:hover:text-gray-300"
                    id="inactive_jobs-tab" data-tabs-target="#inactive_jobs" type="button" role="tab"
                    aria-controls="inactive_jobs" aria-selected="false">Inactive Jobs</button>
            </li>
        </ul>
    </div>
    <div id="myTabContent">
        <div class="hidden px-2 rounded-lg bg-gray-50 dark:bg-gray-800" id="active_jobs" role="tabpanel"
            aria-labelledby="active_jobs-tab">
            <JobsActiveJobs />
        </div>
        <div class="hidden p-4 rounded-lg bg-gray-50 dark:bg-gray-800" id="inactive_jobs" role="tabpanel"
            aria-labelledby="inactive_jobs-tab">
            <JobsInActiveJobs />
        </div>
    </div>
</template>



<script setup>
import { onMounted } from 'vue'
import { initFlowbite } from 'flowbite'

// initialize components based on data attribute selectors
onMounted(() => {
    initFlowbite();
})


</script>