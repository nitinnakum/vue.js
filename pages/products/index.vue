<template>
    <div class="grid lg:grid-cols-6 md:grid-cols-5 sm:grid-cols-4 grid-cols-1">
        <div v-for="(product, index) in products" :key="index" class="p-3">
            <single-product :title="product.title" :price="product.price" :id="product.id" />
            <!-- <ProductsSingleProduct :title="product.title" :price="product.price" :id="product.id" /> -->
        </div>
    </div>

</template>
<script>
import  ComponentProductSingleProduct  from "~/components/products/singleProduct.vue";
export default {
    name:"productIndexPage",
    components: {"single-product":ComponentProductSingleProduct},
    data(){
        return {    
            nitin: "hello i'm nitin",
            products: [
                {
                    id:1,
                    title:"product1",
                    price:200
                },
                {
                    id:2,
                    title:"product2",
                    price:2400
                },
                {
                    id:3,
                    title:"product3",
                    price:3200
                },
                {
                    id:4,
                    title:"product4",
                    price:2007
                },
                {
                    id:5,
                    title:"product5",
                    price:5200
                },
            ],
        }  
    }, 
}
</script>
<style scoped>

</style>