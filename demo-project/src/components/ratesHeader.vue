<template>
  <div class="ratesHeader">
    <img class="editIcon" src="@/assets/header_bg.png"/>
    <input class="originNum" @click="editNumber" type="number"/>>
    <div class="headerBottom">
      <img class="countryIcon"  v-bind:src="currentCountry"></div>
      <p class="unitText">{{unitText}}</p>
      <p class="updateTime">{{updateTime}}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ['updateTime', 'unitText', 'currentCountry', 'currentNumber'],
  data () {
    return {
      updateTime: "更新时间：2018/6/4",
      unitText: "CNY \n 人民币",
      currentCountry: "@/assets/china.png",
      currentNumber: '2'
    }
  },
  methods: {
    editNumber () {
      console.log('edit number');
    }
  }
}
</script>

<style lang="less">
  .ratesHeader {
    position: relative;
    margin: 0;
    padding: 0;
    height: 300px;
    width: 100%;
    background-color: aquamarine;
  }
  .editIcon {
    height: 20px;
    width: 20px;
    position: absolute;
    right: 10px;
    top: 10px;
  }
  .originNum {
    position: relative;
    top: 40px;
    width: 100%;
    height: 220px;
    text-align: center;
    font-size: 40pt;
    line-height: 220px;
    background-color: beige;

  }
  .headerBottom {
    display: flex;
    flex-direction: row;
    position: relative;
    top: 40px;
    margin: 0;
    width: 100%;
    height: 40px;
    background-color: gray;
  }
  .countryIcon {
      background-color: yellow;
      padding: 5px;
      border-radius: 50%;
      margin: 0;
      width: 40px;
      height: 30px;
      left: 10px;
    }
  .unitText {
    margin: 0;
    position: relative;
    font-size: 11pt;
    left: 50px;
    height: 40px;
    width: 70px;
    background-color: brown;
  }
  .updateTime {
    margin: 0 auto;
    position: relative;
    right: 10px;
    top: -20px;
    width: 100%;
    height: 15px;
    font-size: 9pt;
    text-align: right;
    // background-color: blueviolet;
  }
</style>
