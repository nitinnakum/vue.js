<template>
<div v-for="(image, index) in productImage">
    <img :src="image" alt="">
</div>
</template>
<script>
export default{
    name: "componentensProductImage",
    props: {
        productImage : {type : Object}
    }
}
</script>
<style>
</style>