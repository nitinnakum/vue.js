<template>
 <div v-for="(value, key) in singalUser" class="flex gap-3 justify-start mx-4 sm:ml-[44%]">
    <div class="flex items-center text-gray-600 text-xs uppercase sm:text-base">{{ key }}</div> :
    <div class="font-bold text-base text-gray-600 sm:text-lg">{{ value }}</div>
 </div>
</template>
<script>
export default{
    name: "componentsUserDetailList",
    props: {
        singalUser: { type : Object}
    }
}
</script>