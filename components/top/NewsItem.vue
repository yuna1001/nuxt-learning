<script setup lang="ts">
interface NewsItem {
    id: number
    date: string
    category: string
    title: string
    content: string
}

const props = defineProps<{
    newsItem: NewsItem
}>()

</script>

<template>
    <div class="px-10 py-5 flex">
        <div class="mr-3">
            <div>{{ newsItem.date }}</div>
            <div class="text-white text-center"
                :class="{
                    'bg-blue': newsItem.category === 'APP',
                    'bg-green': newsItem.category === 'News'
                }"
            >{{ newsItem.category }}</div>
        </div>
        <div>
            <p>{{ newsItem.title }}</p>
        </div>
    </div>
</template>

<style>
.bg-blue {
    background-color: #386FB2;
}

.bg-green {
    background-color: #6CC100;
}
</style>