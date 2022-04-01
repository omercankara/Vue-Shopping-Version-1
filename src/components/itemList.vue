<template>
        <div class="container">
                <div class="row d-flex justify-content-center py-5">
                        <div class="col-md-12  ">
                                <table class="table text-center">
                                        <thead>
                                                <tr>
                                                        <th>Ürün</th>
                                                         <th>Adet</th>
                                                        <th>Birim Fiyati</th>
                                                        <th>Toplam Fiyat</th>
                                                </tr>
                                              
                                        </thead>
                                        <tbody v-for="item in getItem" :key="item" >
                                                <tr>
                                                        <td class="font-weight-bold">{{item.title}}</td>
                                                        <td class="font-weight-bold">{{item.count}}</td>
                                                        <td class="font-weight-bold">{{item.price}}</td>
                                                        <td class="font-weight-bold">{{item.totalCount}}</td>                              
                                                </tr>
                                        </tbody>
                                     
                                </table>
                                <p class="text-center font-weight-bold">Toplam Fiyat :{{$filters.currencyUSD(toplamFiyat)}} </p>
                        </div>
                </div>
        </div>
</template>


<script>
import {mapGetters} from "vuex"
export default {
       computed:{
           ...mapGetters(['getItem','toplamFiyat','getPrice']),
       },
        data(){
                return{
                       
                }
        },

      watch:{
                toplamFiyat(){
                        if(this.getDatas > 100){
                                 console.log("Tebrikler  Sıfırladınız")
                        
                        }
                },
        
                
                
        
      },
     

        
     
}       
</script>