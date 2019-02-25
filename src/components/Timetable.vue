<template>
  <div id="timetable-container">
    <div id="timetable-title">
      <h1>九九乘法表</h1>
      <p>MULTIPLICATION CHART</p>
    </div>
    <div class="timetable-ele" v-for="index in 8" :key="index">
      <div id="left-col">
        <div class="ele-title">{{ index + 1 }}</div>
        <div class="ele-calculate" v-for="i in 3" :key="i">
          {{ index + 1 }} X {{ i }} = {{ index * i }}
        </div>
      </div>
       <div id="right-col">
        <div class="ele-calculate" v-for="j in 6" :key="j">
          {{ index + 1 }} X {{ j + 3 }} = {{ index * j }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Timetable',
  data() {
    return {
      index: [2, 3, 4, 5, 6, 7, 8, 9, 10],
    };
  },
};
</script>

<style scoped>
#timetable-container {
  display: grid;
  grid-template-columns: auto auto auto;
  justify-content: center;
  grid-gap: 15px;
  padding: 10px;
  background-color: #F0F0F0;
  border-bottom: 30px solid #2EB738;
  margin: 0px 10%;
}

#timetable-title {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  font-family: 'PingFang TC', Medium;
  border-top: 1px solid #2EB738;
  border-bottom: 1px solid #2EB738;
}

#timetable-title > h1{
  font-size: 56px;
  margin: 0px;
}

#timetable-title > p{
  font-size: 24px;
  margin: 0px;
}

.timetable-ele {
  display: flex;
  background-color: #fff;
  border-radius: 100px 0px 30px 0px;
  box-shadow: 0px 3px 10px #D8D8D8;
  width: 320px;
  height: 320px;
  padding: 15px;
}

#left-col {
  display: grid;
  flex: 1;
  margin-right: 5px;
}

#right-col {
  display: grid;
  flex: 1;
}

.ele-title {
  text-align: center;
  font-family: 'Helvetica Neue';
  font-weight: bold;
  font-size: 110px;
}

.ele-calculate {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
