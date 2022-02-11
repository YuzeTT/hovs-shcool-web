<template>
  <div class="navbar">
    <!-- <h3 style="visibility: hidden">HOVS · SCHOOL</h3> -->
    <n-grid cols="3" item-responsive >
      <n-grid-item span="3 700:1" class="title">
        <span>HOVS · SCHOOL</span>
      </n-grid-item>
      <n-grid-item span="3 700:1" class="time_box">
        <div class="time">
          <span>北京时间 <span class="time_num">{{clock.time}}</span></span>
        </div>
      </n-grid-item>
      <n-grid-item span="3 700:1">
        
      </n-grid-item>
    </n-grid>
    <!-- <n-space justify="space-between">
      <h3 class="title">HOVS · SCHOOL</h3>
      <div class="time">
        <h3>北京时间: 15:13:27</h3>
      </div>
      <h3 style="visibility: hidden">HOVS · SCHOOL</h3>
    </n-space> -->
  </div>
</template>

<script setup>
import { reactive } from 'vue';
import { 
  NSpace,
  NGrid,
  NGridItem,
} from 'naive-ui'

const clock = reactive({time:'--:--:--'})

var week = ['SUN', 'MON', 'TUE', 'WED', 'THU', 'FRI', 'SAT'];
var timerID = setInterval(updateTime, 1000);
updateTime();
function updateTime() {
  var cd = new Date();
  clock.time = zeroPadding(cd.getHours(), 2) + ':' + zeroPadding(cd.getMinutes(), 2) + ':' + zeroPadding(cd.getSeconds(), 2);
};

function zeroPadding(num, digit) {
  var zero = '';
  for (var i = 0; i < digit; i++) {
    zero += '0';
  }
  return (zero + num).slice(-digit);
}

</script>

<style lang="scss" scoped>
.navbar {
  padding: 0 15px;
  .title {
    display: flex;
    align-items: center;
    color: white;
    font-size: 1.4rem;
    font-weight: bold;
    span {
      display: flex;
      align-items: center;
      height: 100%;
    }
  }
  .time_box {
    margin: 10px;
    height: 4rem;
    display: flex;
    align-items: center;
    justify-content:center;
    .time {
      color: white;
      // padding: 10px 15px;
      // margin: 15px 15px;
      // line-height: 2rem;
      padding: 10px 15px;
      background-color: rgba($color: #2080F0, $alpha: .3);
      font-size: 1rem;
      border-radius: 5px;
      span {
        font-size: 1.2rem;
        .time_num {
          font-weight: 900;
        }
      }
    }
  }
  
  @media screen and (max-width: 729px) { 
    .navbar {
      padding: 0 5px;
    }
    .title {
      font-size: 1.3rem;
      justify-content: center;
      margin-bottom: 0;
      padding-top: 20px;
    }  
  } 
}
</style>