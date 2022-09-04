<template>
  <div class="container">
    <button @click="changeIsVisible" class="description-button">
      Description
    </button>
    <div class="description-text" v-if="isVisible">
      <p>
        What is a ToDo List? <br>
      </p>
      <p>The definition is a simple one. <br> It’s a list of tasks you need to complete or things that you want to do. </p>
    </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Description",

  data(){
    return{
      isVisible: false
    }
  },

  methods: {
    changeIsVisible(){
      this.isVisible = !this.isVisible
    }
  }
}
</script>

<style scoped>

  .container{
    display: flex;
    flex-direction: column;
    margin: 25px auto;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .description-button{
    background-color: #006064;
    color: white;
    border: 2px solid teal;
    width: 200px;
    height: 48px;
    font-size: 22px;
    padding: 5px;
  }

  .description-button:hover{
    background-color: #025054;
  }

  .description-text{
    background-color: #006064;
    border-radius: 15px;
    margin-top: 30px;
    max-width: 60%;
    padding: 10px;
  }

  .description-text p{
    font-size: 22px;
    color: white;
  }

  p{
    margin-bottom: 12px;
  }
</style>