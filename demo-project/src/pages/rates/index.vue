<template>
  <div>
    <rates-header class="header"></rates-header>
    <ul class="list" v-for="item in items">
      <li class="cell">
        <div>
          <p class="cellTitle">{{item.title}}</p>
          <img class="cellIcon"></img>
          <p class="cellRates">{{item.rates}}</p>
          <div class="cellUnitName">{{item.unit}}</div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
import ratesHeader from "@/components/ratesHeader"
export default {
  data () {
    return {
      items: [{title: '中国', rates: '4.5', unit: '港币1'}, 
      {title: 'HK', rates: '4.5', unit: '美元'}, 
      {title: 'TW', rates: '4.5', unit: '人民币'}, 
      {title: 'US', rates: '4.5', unit: '新台币'}, 
      {title: 'JPN', rates: '4.5', unit: '日元'}, 
      {title: '中国', rates: '4.5', unit: '韩元'}, 
      {title: 'HK', rates: '4.5', unit: '港币'}, 
      {title: 'TW', rates: '4.5', unit: '韩元'}, 
      {title: 'US', rates: '4.5', unit: '港币'}, 
      {title: 'JPN', rates: '4.5', unit: '港币'},
      {title: '中国', rates: '4.5', unit: '港币'}, 
      {title: 'HK', rates: '4.5', unit: '港币'}, 
      {title: 'TW', rates: '4.5', unit: '港币'}, 
      {title: 'US', rates: '4.5', unit: '新台币'}, 
      {title: 'JPN', rates: '4.5', unit: '港币1'}]
    }
  },
 components: {
   ratesHeader
 }
}
</script>

<style lang="less">
.header {
}
.list {
  margin-top: 100px;
}
@cellHeight: 40px;
.cell {
  margin: 0 auto;
  display: flex;
  height: @cellHeight;
  width: 100%;
}
.cellTitle {
  margin-left: 30px;
  background-color: antiquewhite;
  width: 50%;
}
@iconHeight: 25px;
.cellIcon {
  margin-top: @cellHeight/2;
  background-color: yellowgreen;
  width: @iconHeight;
  height: @iconHeight;
  border-radius: @iconHeight/2;
} 

.cellRates {
  margin-left: 100px;
  background-color: azure;
  width: 100%;
}
.cellUnitName {
  background-color: burlywood;
  margin-left: 150px;
  margin-top: -30px;
  width: 100%;
}
</style>

