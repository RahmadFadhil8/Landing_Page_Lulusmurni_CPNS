<template>
    <div :class="['rounded-lg shadow-xs overflow-hidden', cardClass]">
        <slot/>
    </div>
</template>


<script setup lang="ts">
const props = defineProps({
    variant: {
        type: String,
        default: 'white'
    }
})

const cardClass = computed(() => {
    switch (props.variant) {
        case 'Masalah':
            return 'bg-blue-100'
        case 'Solusi':
            return 'bg-orange-100'
        case 'Benefit':
            return 'bg-green-100'
        default:
            return ''
    }
})
</script>