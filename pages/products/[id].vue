<template>
    <div class="grid grid-cols-1 sm:grid-cols-2">
        <div>
            <Product-image :productImage="products[this.$route.params.id].images" />
        </div>
        <div>
            <div>
                {{ products[this.$route.params.id].title }}
                <div>
                    <span>${{ products[this.$route.params.id].price.finalPrice }}</span>
                    <span class="p-3">${{ products[this.$route.params.id].price.mrp }}</span>
                    <span>Flat {{ ((products[this.$route.params.id].price.finalPrice * 100)/ products[this.$route.params.id].price.mrp).toFixed(2) }}% Discount</span>
                </div>
            </div>
            <div>
               <product-details :product="products[this.$route.params.id]"/>     
            </div>
        </div>
    </div>
</template>
<script>
import componentProductDetail from "~/components/products/detail.vue";
import componentensProductImage from "~/components/products/image.vue";
export default {
    computed : {
        pageTitle () {
            return 'test from component'
        }
    },
    name:"productDetailPage",
    components: {"product-details" :componentProductDetail, "Product-image" :componentensProductImage},

    data(){
        return {
            "products" : {
                1:{
                    images:[
                        'https://placehold.co/600x400?text=hello 1', 
                        // 'https://placehold.co/600x400?text=hello+2', 
                        // 'https://placehold.co/600x400?text=hello+3',  
                                  ],
                    title:"SAMSUNG 32 inch 4K Ultra HD LED Backlit VA Panel with 1 Billion Colors, PBP, Slim Bezels Flat Monitor (LU32J590UQWXXL)  (AMD Free Sync, Response Time: 4 ms, 60 Hz Refresh Rate)",
                    price: {
                        finalPrice: 2000,
                        mrp: 3434
                    },
                    details: {
                        "General": {
                            "Model Name": "LU32J590UQWXXL",
                            "Color": "Dark Blue Grey",
                            "Display": "81.28 cm (32 inch) LED Backlit Display",
                            "Backlight": "LED Backlit Backlight",
                            "Panel Type": "VA Panel",
                            "Resolution": "3840 x 2160 pixels",
                            "Screen Resolution Type": "4K Ultra HD",
                            "Sales Package": "1 Monitor, Warranty Card",
                            "Screen Form Factor": "Flat",
                            
                        },
                        "Display Features": {
                            "Maximum Refresh Rate": "60 Hz (Analog)",
                            "Aspect Ratio": "16:09",
                            "Response Time": "4 ms",
                            "Brightness": "270 nits (2D)",
                            "Touchscreen Features": "",
                            "Touchscreen Support": "No",
                            "Power Features": "",
                            "Power Requirement": "AC 100 - 240 V",
                        },
                        "Connectivity": {
                            "HDMI": "Yes",
                        },
                        "Mounting Features": {
                            "Stand": "Simple",
                            "Stand Tilt": "-2 to 20 Degree",
                            "Wall Mounting": "100 x 100 mm",
                        },
                        "Dimensions": {
                            "Width With Stand": "729.5 mm",
                            "Height With Stand": "534.5 mm",
                            "Depth With Stand": "250.5 mm",
                            "Weight With Stand": "6.3 kg",
                            "Width Without Stand": "729.5 mm",
                            "Height Without Stand": "427.8 mm",
                            "Depth Without Stand": "56.4 mm",
                            "Weight Without Stand": "5.5 kg",
                        },
                        
                        "Warranty": {
    
                            "Warranty Summary": "3 Years Warranty",
                            "Covered in Warranty": "Defect Arising Out of Faulty, Defective Material or Workmanship are Covered in Warranty",
                            "Not Covered in Warranty": "Warranty does not Cover Any External Accessories (Such as Battery, Cable, Carrying Bag), Damage Caused to the Product due to Improper Installation by Customer, Normal Wear and Tear to Magnetic Heads, Audio, Video, Laser Pick-ups and TV Picture Tubes, Panel, Damages Caused to the Product by Accident, Lightening, Ingress of Water, Fire, Dropping or Excessive Shock, Any Damage Caused due to Tampering of the Product by An Unauthorised Agent, Liability for Loss of Data, Recorded Images or Business Opportunity Loss",
                            "Domestic Warranty": "3 Year"
                        },
                    }
                },
                2:{
                    images:[
                        // 'https://placehold.co/600x400?text=hello 1', 
                        'https://placehold.co/600x400?text=hello+2', 
                        // 'https://placehold.co/600x400?text=hello+3',      
                              ],
                    title:"SAMSUNG 32 inch 4K Ultra HD LED Backlit VA Panel with 1 Billion Colors, PBP, Slim Bezels Flat Monitor (LU32J590UQWXXL)  (AMD Free Sync, Response Time: 4 ms, 60 Hz Refresh Rate)",
                    price: {
                        finalPrice: 2000,
                        mrp: 3434
                    },
                    details: {
                        "General": {
                            "Model Name": "LU32J590UQWXXL",
                            "Color": "Dark Blue Grey",
                            "Display": "81.28 cm (32 inch) LED Backlit Display",
                            "Backlight": "LED Backlit Backlight",
                            "Panel Type": "VA Panel",
                            "Resolution": "3840 x 2160 pixels",
                            "Screen Resolution Type": "4K Ultra HD",
                            "Sales Package": "1 Monitor, Warranty Card",
                            "Screen Form Factor": "Flat",
                            
                        },
                        "Display Features": {
                            "Maximum Refresh Rate": "60 Hz (Analog)",
                            "Aspect Ratio": "16:09",
                            "Response Time": "4 ms",
                            "Brightness": "270 nits (2D)",
                            "Touchscreen Features": "",
                            "Touchscreen Support": "No",
                            "Power Features": "",
                            "Power Requirement": "AC 100 - 240 V",
                        },
                        "Connectivity": {
                            "HDMI": "Yes",
                        },
                        "Mounting Features": {
                            "Stand": "Simple",
                            "Stand Tilt": "-2 to 20 Degree",
                            "Wall Mounting": "100 x 100 mm",
                        },
                        "Dimensions": {
                            "Width With Stand": "729.5 mm",
                            "Height With Stand": "534.5 mm",
                            "Depth With Stand": "250.5 mm",
                            "Weight With Stand": "6.3 kg",
                            "Width Without Stand": "729.5 mm",
                            "Height Without Stand": "427.8 mm",
                            "Depth Without Stand": "56.4 mm",
                            "Weight Without Stand": "5.5 kg",
                        },
                        
                        "Warranty": {
    
                            "Warranty Summary": "3 Years Warranty",
                            "Covered in Warranty": "Defect Arising Out of Faulty, Defective Material or Workmanship are Covered in Warranty",
                            "Not Covered in Warranty": "Warranty does not Cover Any External Accessories (Such as Battery, Cable, Carrying Bag), Damage Caused to the Product due to Improper Installation by Customer, Normal Wear and Tear to Magnetic Heads, Audio, Video, Laser Pick-ups and TV Picture Tubes, Panel, Damages Caused to the Product by Accident, Lightening, Ingress of Water, Fire, Dropping or Excessive Shock, Any Damage Caused due to Tampering of the Product by An Unauthorised Agent, Liability for Loss of Data, Recorded Images or Business Opportunity Loss",
                            "Domestic Warranty": "3 Year"
                        },
                    }
                },
                3:{
                    images:[
                        // 'https://placehold.co/600x400?text=hello 1', 
                        // 'https://placehold.co/600x400?text=hello+2', 
                        'https://placehold.co/600x400?text=hello+3',                ],
                    title:"SAMSUNG 32 inch 4K Ultra HD LED Backlit VA Panel with 1 Billion Colors, PBP, Slim Bezels Flat Monitor (LU32J590UQWXXL)  (AMD Free Sync, Response Time: 4 ms, 60 Hz Refresh Rate)",
                    price: {
                        finalPrice: 2000,
                        mrp: 3434
                    },
                    details: {
                        "General": {
                            "Model Name": "LU32J590UQWXXL",
                            "Color": "Dark Blue Grey",
                            "Display": "81.28 cm (32 inch) LED Backlit Display",
                            "Backlight": "LED Backlit Backlight",
                            "Panel Type": "VA Panel",
                            "Resolution": "3840 x 2160 pixels",
                            "Screen Resolution Type": "4K Ultra HD",
                            "Sales Package": "1 Monitor, Warranty Card",
                            "Screen Form Factor": "Flat",
                            
                        },
                        "Display Features": {
                            "Maximum Refresh Rate": "60 Hz (Analog)",
                            "Aspect Ratio": "16:09",
                            "Response Time": "4 ms",
                            "Brightness": "270 nits (2D)",
                            "Touchscreen Features": "",
                            "Touchscreen Support": "No",
                            "Power Features": "",
                            "Power Requirement": "AC 100 - 240 V",
                        },
                        "Connectivity": {
                            "HDMI": "Yes",
                        },
                        "Mounting Features": {
                            "Stand": "Simple",
                            "Stand Tilt": "-2 to 20 Degree",
                            "Wall Mounting": "100 x 100 mm",
                        },
                        "Dimensions": {
                            "Width With Stand": "729.5 mm",
                            "Height With Stand": "534.5 mm",
                            "Depth With Stand": "250.5 mm",
                            "Weight With Stand": "6.3 kg",
                            "Width Without Stand": "729.5 mm",
                            "Height Without Stand": "427.8 mm",
                            "Depth Without Stand": "56.4 mm",
                            "Weight Without Stand": "5.5 kg",
                        },
                        
                        "Warranty": {
    
                            "Warranty Summary": "3 Years Warranty",
                            "Covered in Warranty": "Defect Arising Out of Faulty, Defective Material or Workmanship are Covered in Warranty",
                            "Not Covered in Warranty": "Warranty does not Cover Any External Accessories (Such as Battery, Cable, Carrying Bag), Damage Caused to the Product due to Improper Installation by Customer, Normal Wear and Tear to Magnetic Heads, Audio, Video, Laser Pick-ups and TV Picture Tubes, Panel, Damages Caused to the Product by Accident, Lightening, Ingress of Water, Fire, Dropping or Excessive Shock, Any Damage Caused due to Tampering of the Product by An Unauthorised Agent, Liability for Loss of Data, Recorded Images or Business Opportunity Loss",
                            "Domestic Warranty": "3 Year"
                        },
                    }
                }
            }
        }  
    },
    
    
}
</script>
