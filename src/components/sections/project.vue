<template>
    <Container>
      <ProjectCard
        :number="element.number"
        :label="element.label"
        :description="element.description"
        :detail="element.detail"
        :path="element.path"
        :link="element.link"
        :src="element.src"
        v-for="(element, i) in projects"
        :key="i"
      />
    </Container>
  </template>
  
  <script setup lang="ts">
  import Container from '@/components/ui/container.vue';
  import ProjectCard from '@/components/project_card.vue';
  
  import { ref } from 'vue';
  
  const projects = ref([
    { 
      number: "01",
      label: "TOOLS FILES", 
      description: "Nuxt3 | Shadcn | TailwindCSS | InspiraUI | File-comression app using ffmpeg scripts", 
      detail: `
        Our service provides a convenient and fast way to compress files without quality loss. Using powerful FFmpeg-based compression algorithms, we ensure minimal file size while preserving their original resolution and clarity.`,
      path: "https://github.com/vladislav2251/tools.files", 
      src: "/img/tools-files.png",
      link: "https://tools-files.vercel.app/"
    },
    { 
      number: "02",
      label: "AIdea", 
      description: "Nuxt3 | Shadcn | TailwindCSS | InspiraUI | DeepSeek API chat", 
      detail: `
        Talk to an AI that never sleeps, always responds, and sometimes makes more sense than humans `,
      path: "https://github.com/vladislav2251/AIdea", 
      src: "/img/aidea.png",
      link: "https://aidea-r1.vercel.app/"
    },
  ]);
  </script>
  