<script setup>
import AuthenticatedLayout from "@/Layouts/AuthenticatedLayout.vue";
import { Head } from "@inertiajs/vue3";
</script>

<template>
    <Head title="Absensi" />

    <AuthenticatedLayout>
        <div class="pt-6">
            <div class="overflow-x-auto scrollbar-table dark:bg-gray-800">
                <table class="w-full dark:text-white">
                    <thead
                        class="uppercase text-sm border-t border-slate-200 dark:border-slate-700"
                    >
                        <tr class="dark:bg-slate-900/50 text-left">
                            <th class="px-2 py-4 text-center">No</th>
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
