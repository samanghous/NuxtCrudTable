<template>

        <section class="md:flex items-center mb-5">
            <h3 class="text-2xl font-bold md:mr-10 mb-1">7 Active Jobs</h3>
            <p class="text-gray-600 flex items-center mr-10">Sort by:
                <span class="font-bold text-sm text-black flex items-center ml-2">Creation Date
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                        stroke="currentColor" class="w-4 h-4">
                        <path stroke-linecap="round" stroke-linejoin="round"
                            d="M8.25 15L12 18.75 15.75 15m-7.5-6L12 5.25 15.75 9"></path>
                    </svg>
                </span>
            </p>
            <p class="text-gray-600 flex items-center">Status:
                <span class="font-bold text-sm text-black flex items-center ml-2">All Status
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                        stroke="currentColor" class="w-4 h-4">
                        <path stroke-linecap="round" stroke-linejoin="round"
                            d="M8.25 15L12 18.75 15.75 15m-7.5-6L12 5.25 15.75 9"></path>
                    </svg>
                </span>
            </p>
        </section>


    <section class="grid grid-cols-12 gap-4 p-3">
        <JobsJobsCard/>
        <JobsJobsCard/>
        <JobsJobsCard/>
        <JobsJobsCard/>
        <JobsJobsCard/>
        <JobsJobsCard/>
    </section>
    <div>
        
    </div>
</template>