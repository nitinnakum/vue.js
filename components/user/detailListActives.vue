<template>
    <div v-for="(value, key) in data">
        <div class="flex gap-5">
            <div class="m-2 text-sm text-gray-600 font-medium">{{ value.title }}</div>
            <div v-if="(value.states)" class="items-center text-sm text-gray-600 font-medium bg-green-400 w-28 flex justify-center h-8 rounded">
                {{value.states}}
            </div>
        </div>
        <div v-if="value.other" class="font-medium text-sm text-gray-600 mx-5"> {{value.other}}</div>
    </div>
</template>
<script>
export default{
    name : "componentsUserDetailListActives",
    props : {
        data : {type : Object}
    }
}
</script>