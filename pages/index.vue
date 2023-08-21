<script setup lang="ts">
interface NewsItem {
    id: number
    date: string
    category: string
    title: string
    content: string
}

// TODO: 仮データ
const newsItems = ref<NewsItem[]>([
    {
        id: 1,
        date: '2023-08-08',
        category: 'APP',
        title: 'タイトル1タイトル1タイトル1タイトル1タイトル1タイトル1タイトル1タイトル1タイトル1',
        content: 'content1',
    },
    {
        id: 2,
        date: '2023-08-04',
        category: 'News',
        title: 'タイトル2タイトル2タイトル2タイトル2タイトル2タイトル2タイトル2タイトル2タイトル2',
        content: 'content2',
    },
]);
</script>

<template>
    <TopNews :newsItems="newsItems"/>
</template>