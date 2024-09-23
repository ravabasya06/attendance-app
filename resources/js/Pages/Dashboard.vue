<script setup>
import AuthenticatedLayout from "@/Layouts/AuthenticatedLayout.vue";
import Button from "@/Components/PrimaryButton.vue";
import { Head } from "@inertiajs/vue3";
import { ref } from "vue";
const masuk = ref("");
const pulang = ref("");
const masukbtn = () => {
    masuk.value = !masuk.value;
};

const pulangbtn = () => {
    pulang.value = !pulang.value;
};
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
        </div>
        <div class="py-10 flex flex-col justify-center items-center gap-10">
            <span class="dark:text-white text-2xl" v-show="masuk">
                00:00:00 AM</span
            >
            <Button class="dark:text-blue-600 p-2 w-72" @click="masukbtn"
                >ABSEN</Button
            >
            <Button class="dark:text-red-600 p-2 w-72" @click="pulangbtn"
                >PULANG</Button
            >
            <span class="dark:text-white text-2xl" v-show="pulang">
                00:00:00 AM</span
            >
        </div>
    </AuthenticatedLayout>
</template>
