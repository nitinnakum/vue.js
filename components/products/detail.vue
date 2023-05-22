<template>
    <div>
        <h3 class="text-2xl font-bold">Specification</h3>
        <div v-for="(value, key) in product.details">
            <div class="text-lg font-medium">{{ key }}</div>
            <detail-list :singalDetail="value" />
        </div>
    </div>
</template>
<script>
import componentProductDetailList from "~/components/products/detailList.vue";
export default{
    name :'componentProductDetail',
    components: {"detail-list" : componentProductDetailList},
    props:{
        product:{type: Object}
    }
}
</script>