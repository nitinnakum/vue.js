<template>
 <div v-for="(value, key) in singalDetail" class="grid grid-cols-2">
    <span>
        {{ key }}
    </span>

    <span>
        {{ value }}
    </span>

 </div>
</template>
<script>
export default{
    name: "componentProductDetailList",
    props: {
        singalDetail: {type : Object}
    }
}
</script>
<style>
</style>