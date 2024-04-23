<template>
  <div class="header">
    <div>
      標準型電子カルテα版
    </div>
    <div class="headerInfo">
      <div class="headerFactor">
        <button class="peace"><MdiIcon icon="mdiCalendarMonthOutline"/>
          受付一覧</button>
        <button class="peace"><MdiIcon icon="mdiAccountMultiple" />患者一覧</button>
      </div>
      <div class="headerStatus">
        <div class="status"></div>
        <div>オンライン</div>
        <div class="line">|</div>
        <div class="userName">鈴木花子</div>      
        <select name="clinic" id="">
          <option value="">スズキクリニック</option>
          <option value=""></option>
          <option value=""></option>
        </select>
      </div>
    </div>
  </div>
</template>

<script>
</script>

<style scoped>
select {
  padding: 0;
  border: none;
  outline: none;
  font: inherit;
  color: inherit;
  background: none
}
.userName {
  font-weight: bold;
  margin-right: 10px;
}
.header {
  padding: 1.5rem 2rem;
  display: flex;
  background-color: rgb(44, 44, 44);
  color: #fff;
  justify-content: space-between;
  align-items: center;
}
.headerInfo {
  display: flex;
}
.headerFactor {
  display: flex;
}
.headerStatus {
  display: flex;
  
}
.status {
  width:10px;
  height: 10px;
  margin: auto;
  border-radius: 50%;
  background-color: rgb(66, 232, 66);
  
}
.peace {
  margin: auto 35px;
}
.line {
  margin: auto 15px;
}

</style>
