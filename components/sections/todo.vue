<template>
<div class="bg-gray-300 py-20 text-white" >
  <h1 class="text-3xl uppercase text-center pb-20 text-gray-900" >{{ name }}</h1>
  <div class="grid grid-cols-2" >
    <div class="w-72 mx-auto py-72 bg-gray-900 flex flex-col justify-center items-center rounded-lg shadow-lg" >
      <label for="aTodo" class="pb-6 text-2xl">Enter a todo</label>
      <input type="text" name="aTodo" v-model="todoInput" class="p-2 mb-6 text-gray-900">
      <div @click="addTodo()" class="cursor-pointer text-3xl py-2 px-6 bg-yellow-300 rounded-sm" tabindex="0" type="button" ><svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 0 24 24" width="24px" fill="#000000"><path d="M0 0h24v24H0V0z" fill="none"/><path d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"/></svg></div>
    </div>
    <div class="w-72 mx-auto py-72 bg-gray-900 flex flex-col justify-center items-center rounded-lg shadow-lg" >
      <div v-for="todo in todos" :key="todo" >
        {{ todo }}
      </div> 
    </div>
  </div>
</div>
</template>

<script>
export default {
      props:{
        name:{
            type: String,
            required : false,
            default: '名前名とは何ですか？'
        }
    },
  data: () =>({
    todoInput: '',
    todos: []
  }),
  methods:{
    addTodo(){
      if(this.todoInput !== ''){
        this.todos.push(this.todoInput)
        this.todoInput = '' 
      }
    }
  }
}
</script>

<style>

</style>