<template>
    <div>
        <h1 class="text-2xl text-center font-bold text-gray-700">Actinities</h1>
    </div>
    <div v-for="(content, index) in userActivities">
        <div class="text-center font-bold flex m-2 bg-gray-300 gap-3 sm:justify-center">
            <div>
                <img :src="content.icon" alt="" class="w-10">
            </div>
            <div class="flex items-center">
                {{ content.title }}
            </div>
        </div>
        <detailList :data="content.data"/>
        <button class="text-sm flex mx-5 px-3 font-medium rounded bg-gray-200 my-3">View</button>
    </div>
</template>
<script>
import componentsUserDetailListActives from "~/components/user/detailListActives.vue"
export default{
    name : "componentsUserDetailActivities",
    components : {"detailList" : componentsUserDetailListActives},
    props : {
        userActivities : {type : Object}
    }
}
</script>