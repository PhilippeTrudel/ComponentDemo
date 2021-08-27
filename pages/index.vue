<template>
<div>
  <component v-bind:is="component" v-for="component in components" :key="component" />
</div>
</template>

<script>
import Counter from '~/components/sections/counter'
import Todo from '~/components/sections/todo'

export default {
  components:{
    'kek': Counter,
    'kekw' : Todo
  },

  // You can call them by name or by components, even by renaming them
  data: () => ({
    components : ["kek", 'kekw',]
  })
}
</script>
