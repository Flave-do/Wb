<template>
	<header>
		<div class="top">
            <div class="time">
				{{getDay()}}
            </div>
        </div>
		<searchbox/>
		<navTop/>
	</header>
	
</template>

<script>
import searchbox from './searchbox.vue';
import navTop from './navTop'

export default {
	name:'handeTop',
  	components: { searchbox, navTop,},
   	data() {
    	return {
			
		}
   },
   mounted(){

   },
   methods:{
		getDay () {
			var today = new Date()
			var day; var date;
			if (today.getDay() == 0) day = " 星期日"
			if (today.getDay() == 1) day = " 星期一"
			if (today.getDay() == 2) day = " 星期二"
			if (today.getDay() == 3) day = " 星期三"
			if (today.getDay() == 4) day = " 星期四"
			if (today.getDay() == 5) day = " 星期五"
			if (today.getDay() == 6) day = " 星期六"
			date = "您好!今天是:" + (today.getFullYear()) + "年" + (today.getMonth() + 1) + "月" + today.getDate() + "日" + day + "";
			return date 
		},
		doHandleMonth(month) {
			var m = month;
			if (month.toString().length == 1) {
					m = "0" + month;
			}
			return m;
		},
   },
}

</script>

<style lang='css' scoped> 

header{
    width:100%;
    height:180px;
    background-image:url('~@/assets/head.jpg');
}
/* 顶部 */
.top{
    width:1002px;
    height:26px;
    margin:0 auto;
}
.time{
    width:225px;
    height:26px;
    line-height:26px;
    font-size:12px;
    color:#fff;
    float:left;
	
}


</style>

