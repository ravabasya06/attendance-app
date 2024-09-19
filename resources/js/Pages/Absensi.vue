<script setup>
import AuthenticatedLayout from "@/Layouts/AuthenticatedLayout.vue";
import Button from "primevue/button";
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
    <Head title="Absensi" />

    <AuthenticatedLayout>
        <template #header>
            <div class="flex">
                <h2 class="font-semibold text-xl dark:text-gray-200">
                    Absensi
                </h2>
                <h2 class="dark:text-gray-100 text-right ml-auto">
                    {{ currentTime }}
                </h2>
            </div>
        </template>
        <div class="py-6">
            <Button
                class="font-semibold text-xl dark:text-gray-200"
                label="Save"
                icon="pi pi-check"
                iconPos="right"
            />
        </div>
    </AuthenticatedLayout>
</template>
