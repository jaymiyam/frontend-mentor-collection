<script setup>
import Projects from '../projects.json';
import ProjectCard from './ProjectCard.vue';
</script>

<template>
  <section>
    <div class="container">
      <div class="project-grid">
        <ProjectCard
          v-for="project in Projects"
          key="project.id"
          :project="project"
        />
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped></style>
