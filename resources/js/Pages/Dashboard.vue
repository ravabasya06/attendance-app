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
        <template #header>
            <div class="flex">
                <h2 class="font-semibold text-xl dark:text-gray-200">
                    Dashboard
                </h2>
                <h2 class="dark:text-gray-100 text-right ml-auto">
                    {{ currentTime }}
                </h2>
            </div>
        </template>

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
            <div class="flex justify-center m-5">
                <table class="dark:text-gray-100 border text-center">
                    <thead>
                        <tr>
                            <th class="p-12 border">No</th>
                            <th class="p-12 border">Date & Time</th>
                            <th class="p-12 border">Absen Masuk</th>
                            <th class="p-12 border">Absen Pulang</th>
                        </tr>
                    </thead>
                    <tbody>
                        <!-- di bagian absen masuk ganti warna ya, kalau under jam 9 itu biru, diatas jam 9 dan gk masuk jadi merah -->
                        <tr>
                            <td class="p-12 border">1</td>
                            <td class="p-12 border">2024-09-19 09:00</td>
                            <td class="p-12 border bg-blue-500">08:30</td>
                            <td class="p-12 border">18:00</td>
                        </tr>
                        <tr>
                            <td class="p-12 border">2</td>
                            <td class="p-12 border">2024-09-18 09:15</td>
                            <td class="p-12 border bg-red-600">09:00</td>
                            <td class="p-12 border">17:45</td>
                        </tr>
                        <tr>
                            <td class="p-12 border">2</td>
                            <td class="p-12 border">2024-09-17 09:15</td>
                            <td class="p-12 border bg-red-600">09:00</td>
                            <td class="p-12 border">17:45</td>
                        </tr>
                        <tr>
                            <td class="p-12 border">2</td>
                            <td class="p-12 border">2024-09-16 09:15</td>
                            <td class="p-12 border bg-red-600">09:00</td>
                            <td class="p-12 border">17:45</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </AuthenticatedLayout>
</template>
