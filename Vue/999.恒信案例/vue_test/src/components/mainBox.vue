<template>
    <div class="mainbox">
        <leftBox/>
        <rightBox/>
    </div>
</template>
<script>
import leftBox from './leftBox'
import rightBox from './rightBox.vue'
export default {
   name:'mainBox',
   data() {
      return {
      }
   },
   components:{leftBox,rightBox},

   computed:{
   },
   methods:{
   },
}
</script>
<style lang='css' scoped> 
.mainbox{
    width:1002px;
    display:block;
    overflow:hidden;
    margin:0 auto;
    background:#FFF;
}
</style>

