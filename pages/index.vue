<template>
    <div class="md:flex justify-between w-11/12 mx-auto my-5">
        <h4 class="md:text-xl font-bold">Last Changed at: <span class="text-gray-400">5/26/2023, 5:39:53 PM</span></h4>
        <h4 class="md:text-xl font-bold">Total Hours Last 3 Months: <span class="mr-2 text-gray-400">0 Hours</span></h4>
        <h4 class="md:text-xl font-bold"> Total Hours Next 3 Months: <span class="text-gray-400">0 Hours</span></h4>
    </div>

    <div class="w-11/12 mx-auto">
        <div>{{formdata}}</div>
        <div class="mb-10">
            <h2 class="md:text-4xl text-2xl font-bold mb-5">PAST / CONTINUING STAGE</h2>
            <div v-if=!formdata.length class="overflow-x-auto">
                <form><!----></form>
                <form class="flex justify-center mt-5">
                    <button type="submit"
                        class="text-white bg-gradient-to-r from-blue-500 via-blue-600 to-blue-700 hover:bg-gradient-to-br focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center mr-2 mb-2"
                        onclick="generateTable()">
                        <span>
                            Create New Table
                        </span>
                    </button>
                </form>
            </div>
            <div v-if=formdata.length class="overflow-x-auto">
                <form>
                    <table class="w-full text-sm text-left text-gray-500">
                        <thead class="text-xs text-gray-700 bg-gray-50">
                            <tr>
                                <th scope="col" class="px-4 py-3">Work to be done</th>
                                <th scope="col" class="px-4 py-3">Hours Last 3 Months</th>
                                <th scope="col" class="px-4 py-3">Hours Next 3 Months</th>
                                <th scope="col" class="px-4 py-3">Primary Stakeholder</th>
                                <th scope="col" class="px-4 py-3">Outcome</th>
                                <th scope="col" class="px-4 py-3">Skills Required</th>
                                <th scope="col" class="px-4 py-3">Work Quality</th>
                                <th scope="col" class="px-4 py-3">Capability</th>
                                <th scope="col" class="px-4 py-3">Interest</th>
                                <th scope="col" class="px-4 py-3">Comment</th>
                                <th scope="col" class="px-4 py-3">Action</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr class="border-b">
                                <th scope="row" class="px-4 py-3 font-medium text-gray-900 whitespace-nowrap"></th>
                                <td class="px-4 py-3"></td>
                                <td class="px-4 py-3"></td>
                                <td class="px-4 py-3"></td>
                                <td class="px-4 py-3"></td>
                                <td class="px-4 py-3"></td>
                                <td class="px-4 py-3"></td>
                                <td class="px-4 py-3"></td>
                                <td class="px-4 py-3"></td>
                                <td class="px-4 py-3"></td>
                                <td class="text-center">
                                    <div class="flex items-center justify-center"><button class="py-3 text-blue-600"
                                            type="button"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"
                                                fill="currentColor" class="w-6 h-6">
                                                <path
                                                    d="M21.731 2.269a2.625 2.625 0 00-3.712 0l-1.157 1.157 3.712 3.712 1.157-1.157a2.625 2.625 0 000-3.712zM19.513 8.199l-3.712-3.712-8.4 8.4a5.25 5.25 0 00-1.32 2.214l-.8 2.685a.75.75 0 00.933.933l2.685-.8a5.25 5.25 0 002.214-1.32l8.4-8.4z">
                                                </path>
                                                <path
                                                    d="M5.25 5.25a3 3 0 00-3 3v10.5a3 3 0 003 3h10.5a3 3 0 003-3V13.5a.75.75 0 00-1.5 0v5.25a1.5 1.5 0 01-1.5 1.5H5.25a1.5 1.5 0 01-1.5-1.5V8.25a1.5 1.5 0 011.5-1.5h5.25a.75.75 0 000-1.5H5.25z">
                                                </path>
                                            </svg></button><button class="py-3 text-red-600" type="button"><svg
                                                xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"
                                                class="w-6 h-6">
                                                <path fill-rule="evenodd"
                                                    d="M16.5 4.478v.227a48.816 48.816 0 013.878.512.75.75 0 11-.256 1.478l-.209-.035-1.005 13.07a3 3 0 01-2.991 2.77H8.084a3 3 0 01-2.991-2.77L4.087 6.66l-.209.035a.75.75 0 01-.256-1.478A48.567 48.567 0 017.5 4.705v-.227c0-1.564 1.213-2.9 2.816-2.951a52.662 52.662 0 013.369 0c1.603.051 2.815 1.387 2.815 2.951zm-6.136-1.452a51.196 51.196 0 013.273 0C14.39 3.05 15 3.684 15 4.478v.113a49.488 49.488 0 00-6 0v-.113c0-.794.609-1.428 1.364-1.452zm-.355 5.945a.75.75 0 10-1.5.058l.347 9a.75.75 0 101.499-.058l-.346-9zm5.48.058a.75.75 0 10-1.498-.058l-.347 9a.75.75 0 001.5.058l.345-9z"
                                                    clip-rule="evenodd"></path>
                                            </svg></button></div>
                                </td>
                            </tr>
                        </tbody>
                    </table>
                </form>
                <form class="flex justify-center mt-5"><button type="submit"
                        class="text-white bg-gradient-to-r from-blue-500 via-blue-600 to-blue-700 hover:bg-gradient-to-br focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center mr-2 mb-2"><span>Add
                            Row</span></button>
                </form>
            </div>
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

let formdata = [];

function generateTable() {
    const row= ["Service1",2,2,"My Manager","Revenue Generated","core","Service is working well","I am fully capable","Enjoy the service","all ok"];
    formdata=["1","2"];
    console.log(formdata);
}

</script>