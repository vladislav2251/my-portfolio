<template>
        <img 
                :src="props.src" 
                :alt="props.alt" 
                :loading="isAboveTheFold ? 'eager' : 'lazy'" 
                decoding="async"
        >
</template>

<script setup lang="ts">
        import type { IImageProps } from '@/interfaces/image.interface';

        const props = defineProps<IImageProps>();

        
</script>
