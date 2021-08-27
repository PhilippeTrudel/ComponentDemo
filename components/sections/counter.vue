<template>
    <div class="bg-gray-800 py-40" >
        <div class="flex justify-center items-center  text-white flex-col py-20 w-72 mx-auto bg-gray-900 rounded-lg shadow-lg" >
            <h4 class="text-3xl pb-10 uppercase text-center"> {{ title }} </h4>
            <div class="text-9xl pb-10 flex justify-center" >
                {{ count }}
            </div>
            <div class="flex justify-center space-x-8">
                <div @click="decrement()" class="cursor-pointer text-3xl py-2 px-6 bg-yellow-300 rounded-sm" tabindex="0" type="button" >
                    <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 0 24 24" width="24px" fill="#000000"><path d="M0 0h24v24H0V0z" fill="none"/><path d="M19 13H5v-2h14v2z"/></svg>
                </div>
                <div @click="increment()" class="cursor-pointer text-3xl py-2 px-6 bg-yellow-300 rounded-sm" tabindex="0" type="button">
                    <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 0 24 24" width="24px" fill="#000000"><path d="M0 0h24v24H0V0z" fill="none"/><path d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"/></svg>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props:{
        title:{
            type: String,
            required : false,
            default: 'I\'m missing a title #sad'
        }
    },
    data: () => ({
        count: 0
    }),
    methods:{
        increment(){
            this.count++
        },
        decrement(){
            if(this.count > 0){
                this.count--
            }
        }
    }
}
</script>

<style>

</style>