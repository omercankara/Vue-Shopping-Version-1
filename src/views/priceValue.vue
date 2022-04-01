<template>
        <h1 class="text-center"> Bakiyeniz : {{$filters.currencyUSD(getPrice)}}</h1>
</template>

<script>
import { mapGetters } from "vuex";
export default {
computed:{
           ...mapGetters(['getPrice'])
        }       
}
</script>