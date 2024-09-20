<script setup>
import AuthenticatedLayout from "@/Layouts/AuthenticatedLayout.vue";
import { Head } from "@inertiajs/vue3";
</script>

<template>
    <Head title="Users" />

    <AuthenticatedLayout>
        <div class="overflow-x-auto scrollbar-table pt-5">
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
                                <span>created at</span>
                            </div>
                        </th>
                        <th class="px-2 py-4">
                            <div class="flex justify-between items-center">
                                <span>updated at</span>
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
    </AuthenticatedLayout>
</template>
