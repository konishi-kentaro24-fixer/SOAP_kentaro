<template>
  <div class="mainMenu">
    <div class="leftMenu">
      <div><span class="patientName">小西健太郎</span>コニシケンタロウ<span class="patientBirth">25歳0ヶ月|男性</span></div>
      <div>2024年4月27日(土)16:00~17:00</div>
    </div>
    <div class="rightMenu">
      <div class="DrInfo">対面診断|一般内科|スズキクリニック|中村　順子|ID:139690</div>
      <div class="buttonBox">
        <button>クリア</button>
        <button>保存して診断完了</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.mainMenu {
  display: flex;
  justify-content: space-between;
  div.leftMenu > div {
    font-size: 0.6rem;
    span.patientName {
      font-weight: bold;
    }
    span.patientName {
      padding-right: 5px;
    }
    span.patientBirth {
      margin: 5px;
      color: rgb(161, 160, 160);
    }
  }
  div:last-child {
    margin-bottom: 5px;
  }
  div.rightMenu {
    div.DrInfo {
      font-size: 0.6rem;
      color: rgb(161, 160, 160);
      margin-bottom: 0;
    }
    div.buttonBox {
      display: flex;
      justify-content: flex-end;
      button {
        border: 1px solid rgb(161, 160, 160);
        font-size: 0.8rem;
        border-radius: 5px;
        margin-left: 10px;
        margin-top: 10px;
        padding: 5px 20px;
        font-weight: bold;
      }
    }
    .buttonBox > button:first-child {
      background-color: #fff;
    }
    .buttonBox > button:last-child {
      background-color: rgb(42, 179, 191);
      color: #fff;
    }
  }
}
</style>