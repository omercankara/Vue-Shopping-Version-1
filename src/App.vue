<template>
<div id="app">
        <price/>
        <contextItem  :bilgiler="contentItem" />
        <itemList/>
        
</div>
</template>

<script>
import contextItem from "./components/contentItem.vue"
import itemList from "./components/itemList.vue"
import price from "./views/priceValue.vue"

export default {

       components:{
         price,
        contextItem,
        itemList
       },

       data(){
                return{
                    
                }
       }
}
</script>