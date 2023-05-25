<template>
    <div class="mb-4 border-b border-gray-200 dark:border-gray-700">
        <ul class="flex flex-wrap -mb-px text-sm font-medium text-center" id="myTab" data-tabs-toggle="#myTabContent"
            role="tablist">
            <li class="mr-2" role="presentation">
                <button class="inline-block p-4 border-b-2 rounded-t-lg" id="rctment_inbox-tab" data-tabs-target="#rctment_inbox"
                    type="button" role="tab" aria-controls="rctment_inbox" aria-selected="false">RECRUITMENT INBOX</button>
            </li>
            <li class="mr-2" role="presentation">
                <button
                    class="inline-block p-4 border-b-2 border-transparent rounded-t-lg hover:text-gray-600 hover:border-gray-300 dark:hover:text-gray-300"
                    id="work_inbox-tab" data-tabs-target="#work_inbox" type="button" role="tab"
                    aria-controls="work_inbox" aria-selected="false">WORK INBOX</button>
            </li>
        </ul>
    </div>
    <div id="myTabContent">
        <div class="hidden px-2 rounded-lg bg-gray-50 dark:bg-gray-800" id="rctment_inbox" role="tabpanel"
            aria-labelledby="rctment_inbox-tab">
            <InboxRecruitmentJobs />
        </div>
        <div class="hidden p-4 rounded-lg bg-gray-50 dark:bg-gray-800" id="work_inbox" role="tabpanel"
            aria-labelledby="work_inbox-tab">
            <div>work inbox</div>
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