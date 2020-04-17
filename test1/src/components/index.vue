<template>
  <div>
    <div>
      <input type="text" v-model="inputValue" />
      <button @click="handleSubmit">提交</button>
    </div>
    <ul>
      <li v-for="(item,index) of list" :key="index">{{item}}</li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      inputValue: "",
      list: []
    };
  },
  methods: {
    handleSubmit() {
      this.list.push(this.inputValue);
      this.inputValue = "";
    }
  }
};
</script>
<style scoped>
</style>