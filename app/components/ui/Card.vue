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
            return 'bg-card-masalah'
        case 'Solusi':
            return 'bg-card-solusi'
        case 'Benefit':
            return 'bg-card-benefit'
        default:
            return ''
    }
})
</script>