<template>
<div>
  <component v-bind:is="component" />
  <component v-bind:is="component2" />
</div>
</template>

<script>
import Counter from '~/components/sections/counter'
import Todo from '~/components/sections/todo'

export default {
  components:{
    Counter,
    Todo
  },
  data: () => ({
    component: Counter,
    component2: Todo
  })
}
</script>
