<template>

   <div class="right_box">
            <customerCenter/>
            <newsTips/>
            <div class="clear"></div>
            <speciality/>
   </div>

</template>
<script>
import customerCenter from './customerCenter.vue'
import newsTips from './newsTips.vue'
import Speciality from './speciality.vue'
export default {
   name:'rightBox',
   data() {
      return {
      }
   },
   components:{customerCenter,newsTips, Speciality},
   created(){
   },
   computed:{
   },
   methods:{
   },
}
</script>
<style lang='css' scoped> 
.right_box{ width:723px; display:block; overflow:hidden; float:right;}

</style>

