<script setup>
import TextInput from '@/Components/TextInput.vue';
import GroupItem from '@/Components/app/GroupItem.vue';
import { ref } from 'vue';

const searchKeyword = ref('');
</script>

<template>
<TextInput :model-value="searchKeyword" placeholder="Search for groups" class="w-full"/>
<div class="mt-3 flex-1 overflow-auto">
    <div v-if="false" class="text-grey-400 flex text-center">
        You are not in any group
    </div>

    <div v-else>
        <GroupItem image="https://picsum.photos/100"
        title="Laravel Devs"
        description="Lorem ipsum dolor sit amet consectetur, adipisicing elit."
        />
        <GroupItem image="https://picsum.photos/100"
        title="Vue.js Devs"
        description="Lorem ipsum dolor sit amet consectetur, adipisicing elit."
        />
        <GroupItem image="https://picsum.photos/100"
        title="Laravel Devs"
        description="Lorem ipsum dolor sit amet consectetur, adipisicing elit."
        />
        <GroupItem image="https://picsum.photos/100"
        title="Vue.js Devs"
        description="Lorem ipsum dolor sit amet consectetur, adipisicing elit."
        />
        <GroupItem image="https://picsum.photos/100"
        title="Laravel Devs"
        description="Lorem ipsum dolor sit amet consectetur, adipisicing elit."
        />
        <GroupItem image="https://picsum.photos/100"
        title="Vue.js Devs"
        description="Lorem ipsum dolor sit amet consectetur, adipisicing elit."
        />
        <GroupItem image="https://picsum.photos/100"
        title="Laravel Devs"
        description="Lorem ipsum dolor sit amet consectetur, adipisicing elit."
        />
        <GroupItem image="https://picsum.photos/100"
        title="Vue.js Devs"
        description="Lorem ipsum dolor sit amet consectetur, adipisicing elit."
        />
    </div>
</div>
</template>
