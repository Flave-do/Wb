<template>
    <div id="footer">
        <div class="fnav"><a href=''>网站地图</a> | <a href=''>与我们联系</a> | <a
                target="_blank" href="">
                <img src="~@/assets/beian_icon.png"> 皖公网安备 xxxxxxxxx号</a> | <a target="_blank"
                href="http://www.beian.miit.gov.cn/">皖ICP备xxxxxxx号</a>

        </div>
        <div class="copyright">Copyright 2009 安徽省恒信检验检测有限公司 All Rights Reserved. Designed by <a href="http://www.she.com.cn



      " target="_blank">xiaoyang</a> 未经许可 不得转载<br />
            电话:0558-7627628 传真:0558-7627628 邮编:233500 地址:蒙城县庄子大道东纬一路南侧江淮汽车零部件供应巢C10#105 </div>
    </div>
</template>
<script>
export default {
   name:'Fte',
   data() {
      return {
      }
   },
   created(){
   },
   computed:{
   },
   methods:{
   },
}
</script>
<style lang='css' scoped> 
#footer {
    position: relative;
    border-top:2px;
    margin-top: -0px;/*等于footer的高度*/
    height: 100px;
    clear:both;
    background: #f1f1f1;
    }
.fnav{ text-align:center; line-height:30px; padding-top:10px;} .fnav a{ color:#565656;}
.copyright{ width:1002px; height:25px; line-height:25px; font-size:12px; color:#565656; text-align:center; margin:0 auto;}

</style>

