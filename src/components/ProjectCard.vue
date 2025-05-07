<template>
  <Transition
    appear
    enter-from-class="opacity-0"
    leave-to-class="opacity-0"
    enter-active-class="transition ease-out duration-1000 delay-150"
    leave-active-class="transition ease-in duration-1000"
    enter-to-class="opacity-100"
    leave-from-class="opacity-100"
  >
    <article class="project-card">
      <div>
        <a :href="project.demoLink" target="blank">
          <img
            :src="project.imagePath"
            :alt="project.name"
            class="project-image"
          />
        </a>
      </div>
      <div>
        <h2 class="project-name">{{ project.name }}</h2>
        <div class="project-links">
          <a :href="project.demoLink" target="blank">
            <Icon
              icon="material-symbols:monitor-outline"
              width="24"
              height="24"
            />
            <span>demo</span>
          </a>
          <a :href="project.repoLink" target="blank">
            <Icon icon="mingcute:github-line" width="24" height="24" />
            <span>repo</span>
          </a>
        </div>
      </div>
    </article>
  </Transition>
</template>

<script setup>
import { Icon } from '@iconify/vue';
const { project } = defineProps(['project']);
</script>

<style lang="scss" scoped></style>
