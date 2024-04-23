<template>
  <div class="heading">
      <div>主訴・所見</div>
      <select name="" id="">
        <option value="テンプレート">テンプレート</option>
        <option value="テンプレート">テンプレート</option>
        <option value="テンプレート">テンプレート</option>
      </select>
    </div>
    <div class="main">
      <div class="searchFunc">
        <div>
          診察内容を入力してください...
        </div>
        <input type="text" placeholder="✨AIに質問する">
      </div>
      <div class="contentsUpload">
        <div class="contentsIcons">
          <div v-for="uploadIcon in uploadIcons" :key="uploadIcon.name">
            <MdiIcon :icon="uploadIcon.mdiLink" :style="uploadIcon"/>
          </div>
        </div>
      </div>
    </div>
</template>

<script lang="ts" setup>
import uploadIconsList from "~/assets/icons/uploadIcons.json"
import type { Icons } from "~/types/Icons"

const uploadIcons = ref<Icons[]>(uploadIconsList)

const uploadIcon = reactive({
  height: '1rem',
  width: '1rem',
  'font-size': '0.5rem'
})

</script>

<style scoped>
.heading {
  display: flex;
  justify-content: space-between;
  align-items: center;
  div {
    font-weight: bold;
  }
  select {
    padding: 7px 10px;
    font-size: 0.6rem;
    border-radius: 7px;
    font-weight: bold;
  }
}
.main {
  margin-top: 30px;
  .searchFunc {
    div {
      font-size: 0.6rem;
      color: rgb(161, 160, 160)
    }
    input {
      width: 15rem;
      font-size: 0.6rem;
      padding: 3px
    }
  }
  .contentsUpload {
    height: 10rem;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    align-items: center;
    .contentsIcons {
      display: flex;
      box-shadow: 0px 0px 3px 1px rgb(0 0 0 / 15%);
      div {
        display: flex;
        justify-content: center;
        align-items: center;
        margin: 5px;
      }
    }
  }
}
</style>