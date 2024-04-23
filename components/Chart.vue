<template>
  <div class="chartMain">
    <MainMenu />
    <div class="chartButton">
      <div v-for="buttonContent in buttonStatuses" :key="buttonContent.name">
        <button @click="changeVisStatus(buttonContent)">
          <MdiIcon v-if="buttonContent.name==='追加'" icon="mdiPlusCircleOutline"/>
          {{  buttonContent.name }}
          <MdiIcon :style="closeIcon" v-if="buttonContent.visible" icon="mdiClose"/>

        </button>
      </div>
    </div>
    <div class="chartInfo">
      <MedicalPage v-if="buttonStatuses.find(buttonStatus => buttonStatus.name === '医療')?.visible"/>
      <AddPage v-if="buttonStatuses.find(buttonStatus => buttonStatus.name === '追加')?.visible"/>
    </div>
  </div>
</template>

<script setup lang="ts">
import MedicalPage from './chartContents/MedicalPage.vue';
import AddPage from './chartContents/AddPage.vue';

type ButtonStatuses = {
  name: string,
  visible: boolean,
}
const buttonStatuses = ref<ButtonStatuses[]>([
  {
    name: "医療",
    visible: true,
  },
  {
    name: "追加",
    visible: false,
  },
])

const changeVisStatus = (buttonContent: ButtonStatuses) => {
  buttonStatuses.value.forEach(buttonStatus => {
    if (buttonContent.name === buttonStatus.name) {
      buttonStatus.visible = true;
    } else {
      buttonStatus.visible = false;
    }
  });
}

const closeIcon = reactive({
  height: '1rem',
  width: '1rem',
  'font-size': '0.5rem'
})

</script>

<style scoped>
button {
  background-color: #fff;
  color: rgb(42, 179, 191);
  margin-left: 10px;
  border-radius: 15% 15% 0 0;
  padding: 3px 10px 0 10px;
}
.chartMain {
  width: calc(100% - 30rem);
  /* margin:  */
}
.chartInfo {
  background-color: #fff;
  height: 100%;
}
.chartButton {
  display: flex;
  height: fit-content;
}
.mdiClose {
  font-size: 0.5rem;
}

</style>