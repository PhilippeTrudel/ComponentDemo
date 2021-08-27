<template>
<div>
  <component v-bind:is="component.cpn" v-bind="component" v-for="component in components" :key="component.name" />
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
  // you can even pass props to them with the v-bind
  data: () => ({
    components : [{cpn: 'kek', title: 'Counter'}, {cpn: 'kekw', name: 'Todo'},]
  })
}
</script>
