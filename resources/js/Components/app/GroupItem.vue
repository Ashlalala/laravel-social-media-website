<script setup>
    defineProps({
        image: String,
        title: String,
        description: String
    })
</script>

<template>
    <div class="mb-3 cursor-pointer hover:bg-gray-100">
        <div class="flex items-center gap-1 py-2 px-3">
            <img :src="image" class="w-[48px] rounded-full" alt="Group logo">
            <div>
                <h3 class="font-black text-xl">{{ title }}</h3>
                <div class="text-xs text-grey-500">{{ description }}</div>
            </div>
        </div>
    </div>
</template>
