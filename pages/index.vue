<template>
<div>
  <Counter />
  <Todo />
</div>
</template>

<script>
import Counter from '~/components/sections/counter.vue'
import Todo from '~/components/sections/todo.vue'

export default {
  components:{
    Counter,
    Todo
  }
}
</script>
