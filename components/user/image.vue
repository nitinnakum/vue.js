<template>
    <div>
        <div class="relative">
            <iframe :src="userLocation" width="100%" height="400px"></iframe>
            <img class="hidden sm:block w-36 absolute bottom-[-80px] left-28" :src="userProfileImage" alt="">
        </div>
        <div class="flex">
            <img class="w-1/2 m-2 sm:hidden" :src="userProfileImage" alt="">
            <div class="hidden sm:block w-1/2"></div>
            <div class="w-1/2 m-auto sm:h-36 sm:pt-8">
                <div class="text-2xl font-bold sm:text-4xl" v-for="(value, key) in userHadding">
                    <h1 class="text-center text-gray-700 sm:text-start">{{ value }}</h1>
                </div>
                <div class="text-lg font-medium sm:text-xl" v-for="(value, key) in userHaddingName">
                    <h1 class="text-center text-gray-500 font-bold sm:text-start">{{ value }}</h1>
                </div>
            </div>
        </div>
        <div class="flex mx-3 gap-2 items-center sm:mx-12" v-for="(value, key) in userBasicDetails">
            <h2 class="text-xs font-normal text-gray-600 uppercase sm:text-base">{{ key }} :</h2>
            <h2 class="text-base font-bold text-gray-700 sm:text-xl"> {{ value }}</h2>
        </div>
    </div>
</template>
<script>
export default {
    name: "componentsUserImage",
    props: {
        userLocation: { type: String },
        userProfileImage: { type: String },
        userHadding: { type: Object },
        userHaddingName: { type: Object },
        userBasicDetails: { type: Object }
    }
}
</script>
<style></style>