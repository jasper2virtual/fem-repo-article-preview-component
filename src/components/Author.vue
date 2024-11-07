<template>
    <div class="grid grid-cols-[auto_1fr] grid-rows-2 gap-x-4">
        <img :src="'./assets/images/' + avatar"
            class="rounded-full shadow-sm aspect-square h-10 row-span-2 self-center" />
        <span class="self-end text-very-dark-grayish-blue font-bold">{{ authorName }}</span>
        <span class="self-start text-desaturated-dark-blue font-medium">{{ updateDate }}</span>
    </div>
</template>

<script>
export default {
    props: {
        authorName: {
            type: String,
            default: 'no name'
        },
        updateDate: {
            type: String,
            default: 'no date'
        },
        avatar: {
            type: String
        }
    }
}
</script>