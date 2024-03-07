<script setup>
import { ref, computed } from 'vue'
import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue'
import { TabGroup, TabList, Tab, TabPanels, TabPanel } from '@headlessui/vue'
import { usePage } from '@inertiajs/vue3';
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import TabItem from '@/Pages/Profile/Partials/TabItem.vue';
import Edit from '@/Pages/Profile/Edit.vue';

const props = defineProps({
    user: {
        type: Object,
    },
    mustVerifyEmail: {
        type: Boolean,
    },
    status: {
        type: String,
    },
});

const auth = usePage().props.auth;
const isMyProfile = computed(()=>{
    return auth.user && auth.user.id === props.user.id;
})

</script>

<template>
<AuthenticatedLayout>
    <div class="w-[800px] mx-auto h-full overflow-auto">
        <div class="relative">
            <img src="https://imgs.search.brave.com/abbx34mxoOifgpoVUbULPp3OQkJS78j9pvx_UmCr7gU/rs:fit:860:0:0/g:ce/aHR0cHM6Ly9jZG4u/cGl4YWJheS5jb20v/cGhvdG8vMjAxNy8w/MS8wNi8yMy8wMy9z/dW5yaXNlLTE5NTky/MjdfNjQwLmpwZw"
            alt="Profile cover" class="h-[200px] w-full">
            <img src="https://cdn.iconscout.com/icon/free/png-256/free-avatar-370-456322.png?f=webp"
            alt="Profile avatar"
            class="absolute left-[48px] w-[128px] h-[128px] -bottom-[48px]">
        </div>
        <div>
            <TabGroup>
                <TabList class="pl-[200px] flex bg-white">
                    <Tab v-slot="{ selected }" as="template">
                        <TabItem text="About" :selected="selected"/>
                    </Tab>
                    <Tab v-slot="{ selected }" as="template">
                        <TabItem text="Posts" :selected="selected"/>
                    </Tab>
                    <Tab v-slot="{ selected }" as="template">
                        <TabItem text="Followers" :selected="selected"/>
                    </Tab>
                    <Tab v-slot="{ selected }" as="template">
                        <TabItem text="Followings" :selected="selected"/>
                    </Tab>
                </TabList>

                <TabPanels class="mt-2">
                    <TabPanel key="posts" class="">
                        <Disclosure v-slot="{ open }">
                            <div v-if="!open" class="p-4 sm:p-8 bg-white dark:bg-gray-800 shadow sm:rounded-lg
                            relative">
                                <div>
                                    <h2>{{ user.username }}</h2>
                                    <h2>{{ user.name }}</h2>
                                </div>
                                <DisclosureButton v-if="isMyProfile" class="text-blue-500 hover:underline  absolute top-8 right-8">
                                    Edit
                                </DisclosureButton>
                            </div>
                            <DisclosurePanel>
                                <Edit v-if="isMyProfile" :must-verify-email="mustVerifyEmail" :status="status"/>

                            </DisclosurePanel>
                        </Disclosure>
                    </TabPanel>
                    <TabPanel key="posts" class="bg-white p-3 shadow">
                        Posts
                    </TabPanel>
                    <TabPanel key="followers" class="bg-white p-3 shadow">
                        Followers
                    </TabPanel>
                    <TabPanel key="posts" class="bg-white p-3 shadow">
                        Followings
                    </TabPanel>
                </TabPanels>
            </TabGroup>
        </div>
    </div>
</AuthenticatedLayout>
</template>
