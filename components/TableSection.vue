<template>
    <div class="mx-auto flex flex-col items-center justify-center">
        <button v-if="!tableData.length" @click="createTable"
            class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded mx-auto">
            Create Table
        </button>
        <div v-else class="mx-auto flex flex-col items-center justify-center">
            <table class="table-fixed w-full border-collapse border border-gray-800">
                <thead>
                    <tr>
                        <th class="bg-gray-800 text-white py-2 px-4">Work to be done</th>
                        <th class="bg-gray-800 text-white py-2 px-4">Hours Last 3 Months</th>
                        <th class="bg-gray-800 text-white py-2 px-4">Hours Next 3 Months</th>
                        <th class="bg-gray-800 text-white py-2 px-4">Primary Stakeholder</th>
                        <th class="bg-gray-800 text-white py-2 px-4">Outcome</th>
                        <th class="bg-gray-800 text-white py-2 px-4">Actions</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="(row, index) in tableData" :key="index">
                        <td v-if="editableRow !== index" class="border border-gray-800 py-2 px-4">{{ row.field1 }}</td>
                        <td class="overflow-hidden border border-gray-800" v-else>
                            <select v-model="row.field1" class="mx-7 py-2 px-4">
                                <option value="Select 1">Select 1</option>
                                <option value="Select 2">Select 2</option>
                            </select>
                        </td>
                        <td v-if="editableRow !== index" class="border border-gray-800 py-2 px-4">{{ row.field2 }}</td>
                        <td class="overflow-hidden border border-gray-800" v-else><input v-model="row.field2"
                                class="border border-gray-800 py-2 px-4"></td>
                        <td v-if="editableRow !== index" class="border border-gray-800 py-2 px-4">{{ row.field3 }}</td>
                        <td class="overflow-hidden border border-gray-800" v-else><input v-model="row.field3"
                                class="border border-gray-800 py-2 px-4"></td>
                        <td v-if="editableRow !== index" class="border border-gray-800 py-2 px-4">{{ row.field4 }}</td>
                        <td class="overflow-hidden border border-gray-800" v-else>
                            <select  v-model="row.field4" class="mx-7 py-2 px-4">
                                <option value="Select 1">Select 1</option>
                                <option value="Select 2">Select 2</option>
                            </select>
                        </td>
                        <td v-if="editableRow !== index" class="border border-gray-800 py-2 px-4">{{ row.field5 }}</td>
                        <td class="overflow-hidden border border-gray-800" v-else>
                            <select v-model="row.field5" class="mx-7 py-2 px-4">
                                <option value="Select 1">Select 1</option>
                                <option value="Select 2">Select 2</option>
                            </select>
                        </td>
                        <td v-if="editableRow === null" class="border border-gray-800 py-2 px-4">
                            <button @click="deleteRow(index)"
                                class="bg-red-500 hover:bg-red-700 text-white font-bold py-2 px-4 rounded mr-2">
                                Delete
                            </button>
                            <button @click="editRow(index)"
                                class="bg-green-500 hover:bg-green-700 text-white font-bold py-2 px-4 rounded">
                                Edit
                            </button>
                        </td>
                        <td v-else class="border border-gray-800 py-2 px-4">
                            <button @click="updateRow(index)"
                                class="bg-green-500 hover:bg-green-700 text-white font-bold py-2 px-4 rounded mx-auto">Update</button>
                        </td>
                    </tr>
                </tbody>
            </table>
            <button @click="addRow"
                class="mx-auto my-3 bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
                Add Row
            </button>
        </div>


    </div>
</template>
<script>
export default {
    data() {
        return {
            tableData: [],
            editableRow: null,
        };
    },
    methods: {
        createTable() {
            this.tableData.push({
                field1: 'Select 1',
                field2: '2 Hours',
                field3: '4 Hours',
                field4: 'Select 1',
                field5: 'Select 1'
            });
        },
        deleteRow(index) {
            this.tableData.splice(index, 1);
            if (this.tableData.length === 0) {
                this.editableRow = null;
            }
        },
        editRow(index) {
            this.editableRow = index;
        },
        updateRow(index) {
            this.editableRow = null;
        },
        addRow() {
            this.tableData.push({
                field1: 'Select 1',
                field2: '2 Hours',
                field3: '4 Hours',
                field4: 'Select 1',
                field5: 'Select 1'
            });
        }
    }
};
</script>
<style scoped></style>  