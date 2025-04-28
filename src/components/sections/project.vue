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
      label: "DASHBOARD", 
      description: "Nuxt3 | Shadcn | TailwindCSS | Supabase | CRM Dashboard", 
      detail: `
        dashboard for managing customers and orders, Authentication with Github, Kanban board for tasks, and more`,
      path: "https://github.com/vladislav2251/nuxt-shadcn-dashboard-starter", 
      src: "/img/dashboard.png",
      link: "https://nuxt-shadcn-dashboard-starter.vercel.app/"
    },
    { 
      number: "03",
      label: "NESTJS MONOBANK", 
      description: "Nuxt3 | Shadcn | TailwindCSS | NestJs | Turbo Repo", 
      detail: `
        I developed the front-end part of the website. A simple and convenient solution for integrating the Monobank payment system into your NestJS application. Use this module to create and manage invoices, check statuses, cancel invoices, and implement other payment scenarios with maximum ease.`,
      path: "https://github.com/vladislav2251/nestjs-monobank", 
      src: "/img/mono.png",
      link: "https://nestjs-monobank.vercel.app/"
    },
  ]);
  </script>
  