<script setup>
import AuthenticatedLayout from "@/Layouts/AuthenticatedLayout.vue";
import { Head } from "@inertiajs/vue3";
</script>

<template>
    <Head title="Jam Masuk" />

    <AuthenticatedLayout>
        <div class="dark:bg-slate-700">
            <div class="pt-6">
                <div class="overflow-x-auto scrollbar-table dark:bg-gray-800">
                    <table class="w-full dark:text-white">
                        <thead
                            class="uppercase text-sm border-t border-slate-200 dark:border-slate-700"
                        >
                            <tr class="dark:bg-slate-900/50 text-left">
                                <th class="px-2 py-4 text-center">No</th>
                                <th class="px-2 py-4">
                                    <div
                                        class="flex justify-between items-center"
                                    >
                                        <span>keterangan</span>
                                    </div>
                                </th>
                                <th class="px-2 py-4">
                                    <div
                                        class="flex justify-between items-center"
                                    >
                                        <span>jam mulai</span>
                                    </div>
                                </th>
                                <th class="px-2 py-4">
                                    <div
                                        class="flex justify-between items-center"
                                    >
                                        <span>jam selesai</span>
                                    </div>
                                </th>
                                <th class="px-2 py-4">
                                    <div
                                        class="flex justify-between items-center"
                                    >
                                        <span>aksi</span>
                                    </div>
                                </th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr
                                class="border-t border-slate-200 dark:border-slate-700 hover:bg-slate-200/30 hover:dark:bg-slate-900/20"
                            >
                                <td
                                    class="whitespace-nowrap py-4 px-2 sm:py-3 text-center"
                                >
                                    1
                                </td>
                                <td class="whitespace-nowrap py-4 px-2 sm:py-3">
                                    <span
                                        class="flex justify-start items-center"
                                    >
                                        Jam Masuk
                                    </span>
                                </td>
                                <td class="whitespace-nowrap py-4 px-2 sm:py-3">
                                    07:00
                                </td>
                                <td class="whitespace-nowrap py-4 px-2 sm:py-3">
                                    09:30
                                </td>
                                <td class="whitespace-nowrap py-4 px-2 sm:py-3">
                                    <span
                                        class="border-solid border-2 p-1 border-sky-600 dark:text-sky-600 hover:border-sky-300 hover:dark:text-sky-300 cursor-pointer"
                                    >
                                        edit
                                    </span>
                                </td>
                            </tr>
                            <tr
                                class="border-t border-slate-200 dark:border-slate-700 hover:bg-slate-200/30 hover:dark:bg-slate-900/20"
                            >
                                <td
                                    class="whitespace-nowrap py-4 px-2 sm:py-3 text-center"
                                >
                                    2
                                </td>
                                <td class="whitespace-nowrap py-4 px-2 sm:py-3">
                                    <span
                                        class="flex justify-start items-center"
                                    >
                                        Jam pulang
                                    </span>
                                </td>
                                <td class="whitespace-nowrap py-4 px-2 sm:py-3">
                                    17:00
                                </td>
                                <td class="whitespace-nowrap py-4 px-2 sm:py-3">
                                    21:00
                                </td>
                                <td class="whitespace-nowrap py-4 px-2 sm:py-3">
                                    <span
                                        class="border-solid border-2 p-1 border-sky-600 dark:text-sky-600 hover:border-sky-300 hover:dark:text-sky-300 cursor-pointer"
                                    >
                                        edit
                                    </span>
                                </td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>
        </div>
    </AuthenticatedLayout>
</template>
