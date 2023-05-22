<template>
    <div class="justify-center flex flex-col">
        <img src="https://placehold.co/200x200"/>
        <NuxtLink :to="'/products/'+id">
            <h4 class="title text-1xl text-center">{{  title  }}</h4>
        </NuxtLink>

        <div class="flex justify-center">
            <span class="price text-sm font-bold    "> $ {{ price }}</span>
            <span class="price text-sm line-through px-1"> $ {{ (price+(price*20/100)) }}</span>
            <span class="price text-xs text-green-600"> 20% Off</span>
        </div>
        <button class="btn  bg-orange-500 text-white rounded-full	">Add to cart</button>
    </div>
</template>
<script>
    export default{
        name: "ComponentProductSingleProduct",
        props: {
            id: {type: Number},
            title: {type:String},
            price: {type:Number}
        }  
    }
</script>
<style scoped>
</style>