<template>
    <NuxtLink to="#Paket">
        <div :class="['rounded-lg', buttonClass, full ? 'w-full' : 'w-fit']">
            <slot />
        </div>
    </NuxtLink>
</template>

<script setup lang="ts">
const props = defineProps({
    variant: {
        type: String,
        default: 'white'
    },
    full: {
        type:Boolean,
        default: false
    }
})

const buttonClass = computed(() => {
    switch (props.variant) {
        case 'outline':
            return 'border-2 border-primary text-text-secondary py-3 text-center font-semibold hover:bg-hover/10 transition duration-300 '
        default:
            return 'px-4 py-2 bg-primary hover:bg-hover'
    }
})
</script>