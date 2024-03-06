<script setup>
import TextInput from '@/Components/TextInput.vue';
import FollowingItem from '@/Components/app/FollowingItem.vue';
import { ref } from 'vue';

const searchKeyword = ref('');
</script>

<template>
<TextInput :model-value="searchKeyword" placeholder="Search for groups" class="w-full"/>
<div class="mt-3 flex-1 overflow-auto">
    <div v-if="false" class="text-grey-400 flex text-center">
        You dont have friends yet.
    </div>

    <div v-else>
        <FollowingItem image="https://picsum.photos/100"
        nameFull="John Doe"
        description="Lorem ipsum dolor sit amet consectetur, adipisicing elit."
        />
        <FollowingItem image="https://picsum.photos/100"
        nameFull="Elon Musk"
        description="Lorem ipsum dolor sit amet consectetur, adipisicing elit."
        />
        <FollowingItem image="https://picsum.photos/100"
        nameFull="John Doe"
        description="Lorem ipsum dolor sit amet consectetur, adipisicing elit."
        />
        <FollowingItem image="https://picsum.photos/100"
        nameFull="Elon Musk"
        description="Lorem ipsum dolor sit amet consectetur, adipisicing elit."
        />
        <FollowingItem image="https://picsum.photos/100"
        nameFull="John Doe"
        description="Lorem ipsum dolor sit amet consectetur, adipisicing elit."
        />
        <FollowingItem image="https://picsum.photos/100"
        nameFull="Elon Musk"
        description="Lorem ipsum dolor sit amet consectetur, adipisicing elit."
        />
    </div>
</div>
</template>
