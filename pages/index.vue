<template>
<div>
  <div @click="switchComponent()" class="cursor-pointer text-sm text-center py-2 px-6 bg-yellow-300 rounded-sm" tabindex="0" type="button" >swap component</div>
  <keep-alive>
    <component :is="activeComponent.cpn" v-bind="activeComponent" />
  </keep-alive>
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
    components : [{cpn: 'kek', title: 'Counter'}, {cpn: 'kekw', name: 'Todo'}],
    component: 0
  }),
  methods:{
    switchComponent(){
      this.component++
    }
  },
  computed:{
    activeComponent(){
      return this.components[this.component%2]
    }
  }
}
</script>
