<template>
  <div class="container">

    <h2 class="titleText">Your Tasks:</h2>

    <div  class="scroll-menu">
      <ol>
        <li
            v-for="task in tasks" :key="task.text"
            :class="{'strike': task.isDone}"
            @click="task.isDone = !task.isDone">
          {{task.text}} <img @click="deleteTask(task.text)" :src="image">
        </li>

      </ol>
    </div>

    <input v-model="taskInField" class="textField" @keyup.enter="addTask">
    <button @click="addTask" class="buttonAddTask">add</button>

  </div>
</template>

<script>

import image from '/src/assets/img/delete.svg'

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Functional",

  data(){
    return{
      tasks: [
        {text: 'html', isDone: true},
        {text: 'css', isDone: true},
        {text: 'java script', isDone: false}
      ],

      taskInField: ' ',

      image: image
    }
  },

  methods: {
    addTask(){
      if (this.taskInField !== ' ' && this.tasks.length !== 15){
        this.tasks.push({
          text: this.taskInField,
          isDone: false
        });
        this.taskInField = ''
      }
    },

    deleteTask(taskText){
      this.tasks = this.tasks.filter(task =>{
        return task.text !== taskText
      })


    }
  }

}
</script>

<style scoped>
  .container{
    background-color: teal;
    border-radius: 25px;
    width: 550px;
    height: 500px;
    margin: 40px auto;
    padding-top: 30px;
  }

  .scroll-menu{
    margin: 0 auto;
    border: 3px solid white;
    padding-top: 20px;
    padding-left: 80px;
    color: white;
    font-size: 38px;
    width: 500px;
    height: 300px;
    overflow-y: scroll;
  }

  .scroll-menu li{
    margin-bottom: 10px;
  }

  .textField{
    margin-top: 15px;
    margin-left: 23px;
    width: 350px;
    height: 40px;
  }

  .buttonAddTask{
    height: 40px;
    width: 140px;
    margin-left: 10px;
    color: white;
    font-size: 20px;
    border-style: none;
    background-color: #006064;
  }

  .buttonAddTask:hover{
    background-color: #025054;
  }

  .titleText{
    font-size: 38px;
    color: white;
    margin-left: 180px;
    margin-bottom: 20px;
  }

  .strike{
    text-decoration: line-through black;
  }

</style>