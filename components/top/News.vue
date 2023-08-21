<script setup lang="ts">
interface NewsItem {
    id: number
    date: string
    category: string
    title: string
    content: string
}

const props = defineProps<{
    newsItems: NewsItem[]
}>()

</script>

<template>
    <div class="p-5">
        <div class="flex items-end">
            <div class="flex items-end">
                <h1 class="font-medium text-4xl tracking-wide">News</h1>
                <p>お知らせ</p>
            </div>
            <div class="items-end">
                <ul class="flex items-end border-b-2 mr-0">
                    <!-- TODO リンク先 -->
                    <li><NuxtLink to="/">すべて</NuxtLink></li>
                    <li><NuxtLink to="/">ニュース</NuxtLink></li>
                    <li><NuxtLink to="/">アプリリリース</NuxtLink></li>
                    <li><NuxtLink to="/">IR情報</NuxtLink></li>
                </ul>
            </div>
        </div>

        <div>
            <div v-for="newsItem in newsItems">
                <NuxtLink to="/"><TopNewsItem :newsItem="newsItem" /></NuxtLink>
            </div>
        </div>
    </div>
</template>

<style>
ul li {
    margin-right: 20px;
}
</style>