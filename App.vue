<script>
export default {
  data() {
    return {
      weight: 0,
      height: 0
    };
  },
  computed: {
    bmi() {
      if (this.weight && this.height) {
        return (this.weight / (this.height ** 2));
      }
      return 0;
    }
  }
};
</script>

<template>
  <center>
   <div id="app" class="container">
    <div class="holder">

      <h1>BMI Calculator</h1>
      <div>
        <label for="weight">Weight (kg):</label>
        <input type="number" id="weight" v-model="weight"><br>
        <br>
      </div>
      <div>
        <label for="height">Height (m):</label>
        <input type="number" id="height" v-model="height"><br>
      </div>
      <p>Your BMI result is: {{ bmi }}</p>
    </div>
  </div>
</center>
  </template>

<style scoped>

.container{
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  box-shadow: 1solid;
  width: 400px;
  height: 400px;
}


 input{
  border: none;
  outline: none;
  text-decoration: none;
  justify-content: center;
  align-items: center;
 }
</style>
