<template>
  <div class="heading">
      <div>処置・行為</div>
      <button>セット登録<MdiIcon :icon="mdiPlusCircle" :style="registerButton"/></button>
    </div>
    <div class="main">
      <div class="order">
        <div class="orderChoose"></div>
        <div class="orderOps"></div>
      </div>
    </div>
</template>

<script lang="ts" setup>

// const registerButton = reactive({
//   height: '1rem',
//   width: '1rem',
//   'font-size': '1rem'
// })

</script>

<style scoped>
.heading {
  display: flex;
  justify-content: space-between;
  align-items: center;
  div {
    font-weight: bold;
  }
  button {
    padding: 7px 10px;
    font-size: 0.6rem;
    border-radius: 7px;
    font-weight: bold;
    border: 1px solid rgb(161, 160, 160);
  }
  .main {
    margin-top: 30px;
    /* .order {
      height: 10rem;
      background-color: gray;
    } */
  }
}
</style>