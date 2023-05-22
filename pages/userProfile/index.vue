<template>
    <div class="border border-black border-solid m-5">
        <div v-for="(user, index) in userDetail" :key="index">
            <single-user :id="user.id" :title="user.title"/>
        </div>
    </div>
    </template>
<script>
import componentsUserProfileShow from "~/components/user/ProfileShow.vue"
export default {
    name: "userProfileIndexPage",
    components: {"single-user" : componentsUserProfileShow},
    data() {
        return {
            userDetail:[
                {
                    id: 1,
                    title: "Nitin"
                },
                {
                    id: 2,
                    title: "Chirag"
                },
                {
                    id: 3,
                    title: "Dhaval"
                },
                {
                    id: 4,
                    title: "Ravi"
                }
            ]
        }
    }
}
</script>
<style></style>