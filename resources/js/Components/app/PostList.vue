<script setup>
import PostItem from '@/Components/app/PostItem.vue';
//import TextInput from '@/Components/TextInput.vue';
//import { ref } from 'vue';
//const searchKeyword = ref('');

const post1={
    user: {
        id: 1,
        avatar: 'https://randomuser.me/api/portraits/men/39.jpg',
        name: 'John Smith'
    },
    group: null,
    attachments: [
        {
            id: 1,
            name: 'test.png',
            url: 'https://picsum.photos/1000',
            mime: 'image/png'
        },
        {
            id: 2,
            name: 'test2.png',
            url: 'https://picsum.photos/1000',
            mime: 'image/png'
        },
        {
            id: 3,
            name: 'test3.png',
            url: 'https://picsum.photos/1000',
            mime: 'image/png'
        },
        {
            id: 4,
            name: 'test4.png',
            url: 'https://picsum.photos/1000',
            mime: 'image/png'
        },
        {
            id: 5,
            name: 'test5.png',
            url: 'https://picsum.photos/1000',
            mime: 'image/png'
        },
        {
            id: 6,
            name: 'test6.png',
            url: 'https://picsum.photos/1000',
            mime: 'document/doc'
        }
    ],
    currentActiveAttachment: 0,
    body: `<p>1Lorem ipsum hutwe jdi ouhwoufhowf hufwiuwie iuwediuhdw
        iuwhfiuheihewiufdhewihfd
        oewfowijedoewijdwed
        odiwjowjdoijdwoidjdwdjwdo. </p>
        <p>Lorem ipsum hutwe jdi ouhwoufhowf hufwiuwie iuwediuhdw
        iuwhfiuheihewiufdhewihfd
        oewfowijedoewijdwed
        odiwjowjdoijdwoidjdwdjwdo. </p>
        `,
        created_at: '2024-02-01 07:21'
}
const post2={
    user: {
        id: 2,
        avatar: 'https://randomuser.me/api/portraits/men/33.jpg',
        name: 'Elon Musk'
    },
    group: {
        id: 1,
        name: "Laravel Dev's"
    },
    body: `<p>Lorem ipsum hutwe jdi ouhwoufhowf hufwiuw</p>`,
        created_at: '2024-02-01 09:24'
}
</script>

<template>
    <div class="overflow-auto">
        <PostItem :post="post1"/>
        <PostItem :post="post2"/>
    </div>
</template>

