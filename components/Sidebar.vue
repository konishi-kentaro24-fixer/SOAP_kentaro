<template>
  <div class="sidebar">
    <div class="sidebarIcon">
      <div v-for="sidebarIcon in sidebarIcons" :key="sidebarIcon.name">
        <MdiIcon :icon="sidebarIcon.mdiLink" class="mdiIcon"/>
      </div>
    </div>
    <div class="sidebarMain">
      <div>
        小西健太郎<span class="space"></span>コニシケンタロウ
      </div>
      <hr>
      <div>
        診察記録
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue'
import sidebarIconsList from "~/assets/icons/sidebarIcons.json"
import type { Icons } from '~/types/Icons';


const sidebarIcons = ref<Icons[]>(sidebarIconsList)

</script>

<style scoped>
.sidebar {
  display: flex;
}
.sidebarIcon {
  background-color: rgb(44, 44, 44);
  height: 80vh;
  width: 3rem;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.sidebarIcon div {
  margin-top: 0.5rem;
  height: 2.0rem;
  /* width: 0.5rem; */
}
.mdiIcon {
  font-size: 2rem;
  filter: brightness(0) invert(1);
}
.sidebarMain {
  background-color: white;
  width: 17rem;
  padding-left: 1rem;
}
.space {
  margin: 0.5rem;
}
</style>
