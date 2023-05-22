<template>
        <div v-for="(value, key) in details">
            <div class="text-xl font-medium text-center my-5 bg-gray-300">{{ key }}</div>
            <singalUser :singalUser="value" />
        </div>
</template>
<script>
import componentsUserDetailList from "~/components/user/detailList.vue"
export default {
    name: "componentUserDetail",
    components : {"singalUser" : componentsUserDetailList},
    props: {
        details: {type: Object},
        detailsActivitiesDevices : {type : Object},
        detailsAddtionalActivities : {type : Object}
    }
}
</script>