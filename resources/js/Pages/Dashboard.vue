<script setup>
import AuthenticatedLayout from "@/Layouts/AuthenticatedLayout.vue";
import { Head } from "@inertiajs/vue3";
import { ref, onMounted } from "vue";

const currentTime = ref("");

const updateTime = () => {
    const now = new Date();
    currentTime.value = now.toLocaleString();
};

onMounted(() => {
    updateTime();
    setInterval(updateTime, 1000);
});
</script>

<template>
    <Head title="Dashboard" />

    <AuthenticatedLayout>
        <div class="py-6">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div
                    class="dark:bg-gray-800 overflow-hidden shadow-sm sm:rounded-lg"
                >
                    <div
                        class="font-bold p-6 dark:text-gray-100 text-center text-xl"
                    >
                        Jangan lupa absen!
                    </div>
                </div>
            </div>
            <div class="overflow-x-auto scrollbar-table pt-5">
                <table class="w-full dark:text-white">
                    <thead
                        class="uppercase text-sm border-t border-slate-200 dark:border-slate-700"
                    >
                        <tr class="dark:bg-slate-900/50 text-left">
                            <th class="px-2 py-4 text-center"></th>
                            <th class="px-2 py-4 text-center">#</th>
                            <th class="px-2 py-4">
                                <div class="flex justify-between items-center">
                                    <span>username</span>
                                </div>
                            </th>
                            <th class="px-2 py-4">
                                <div class="flex justify-between items-center">
                                    <span>email</span>
                                </div>
                            </th>
                            <th class="px-2 py-4">
                                <div class="flex justify-between items-center">
                                    <span>absen masuk</span>
                                </div>
                            </th>
                            <th class="px-2 py-4">
                                <div class="flex justify-between items-center">
                                    <span>absen pulang</span>
                                </div>
                            </th>
                            <th class="px-2 py-4 sr-only">Action</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr
                            class="border-t border-slate-200 dark:border-slate-700 hover:bg-slate-200/30 hover:dark:bg-slate-900/20"
                        >
                            <td
                                class="whitespace-nowrap py-4 px-2 sm:py-3 text-center"
                            >
                                <input
                                    class="rounded dark:bg-slate-900 border-slate-300 dark:border-slate-700 text-primary dark:text-primary shadow-sm focus:ring-primary/80 dark:focus:ring-primary dark:focus:ring-offset-slate-800 dark:checked:bg-primary dark:checked:border-primary"
                                    type="checkbox"
                                />
                            </td>
                            <td
                                class="whitespace-nowrap py-4 px-2 sm:py-3 text-center"
                            >
                                1
                            </td>
                            <td class="whitespace-nowrap py-4 px-2 sm:py-3">
                                <span class="flex justify-start items-center">
                                    username
                                </span>
                            </td>
                            <td class="whitespace-nowrap py-4 px-2 sm:py-3">
                                email
                            </td>
                            <td class="whitespace-nowrap py-4 px-2 sm:py-3">
                                00:00
                            </td>
                            <td class="whitespace-nowrap py-4 px-2 sm:py-3">
                                00:00
                            </td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </AuthenticatedLayout>
</template>
