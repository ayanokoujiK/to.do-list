<template>
  <div class="container">
    <h1 class="titleText">To Do List</h1>
    <div class="icon"><img :src='icon'></div>
  </div>
</template>

<script>

import icon from '../assets/img/task.svg';

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Header",
  
  data(){
    return{
      icon: icon
    }
  }
}
</script>

<style scoped>
.container{
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #006064;
  width: 100%;
  height: 10vh;
}

.titleText{
  color: white;
  font-size: 32px;
}

.icon{
  height: 52px;
  width: 52px;

}
</style>