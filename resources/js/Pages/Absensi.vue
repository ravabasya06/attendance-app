<script setup>
import AuthenticatedLayout from "@/Layouts/AuthenticatedLayout.vue";
import Button from "@/Components/PrimaryButton.vue";
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
        <div class="py-10 flex flex-col justify-center items-center gap-10">
            <Button class="dark:text-blue-600 p-2 w-72">ABSEN</Button>
            <Button class="dark:text-red-600 p-2 w-72">PULANG</Button>
        </div>
    </AuthenticatedLayout>
</template>
