<template>
    <div class="flex m-5 gap-5 justify-center">
        <h2 class="text-lg font-semibold">Hi I am {{ title }} Show My Profile ---></h2>
        <NuxtLink :to="'/userProfile/'+title">
            <button class="p-2 w-40 text-lg font-medium bg-yellow-500 rounded-2xl">{{ title }}</button>
        </NuxtLink>
    </div>
</template>
<script>
export default{
    name: "componentsUserProfileShow",
    props: {
        id: {type : Number},
        title: {type : String}
    }
}
</script>
<style>
</style>