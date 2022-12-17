<template>
    <div class="news">
        <slideShow/>
        <!--动态-->
        <div class="dongtai">
            <div class="title3">
                <h1 class="hovers" :id="'one'+p.id"  v-for="p in dyState" :key="p.id" @mouseover="mouseover(p.id)">
                    <a href=''>{{p.title}}</a>
                </h1>
            </div>

            <div :id="'con_one'+(p.id-10)" v-for="p in tipsNew" :key="p.id" :style="showOf(p.id-10)">
                <div class="topNews">
                    <h1><a href=''  :title='p.tips' target="_blank">{{p.target}}</a></h1>
                            <p> {{p.targetP}}<a href=''>[详细]</a> </p>
                </div>
                <ul class="list2">
                    <li v-for="x in p.toSpan" :key="x.id">
                        <span>2021-12-22</span>
                        <a href='' :title="x.title" target="_blank">{{x.target}}</a>
                    </li>
                </ul>
            </div>

        </div>
    </div>

</template>

<script>
import slideShow from './slideShow.vue'
export default {
   data() {
       return {
        dyState:[
            {id:'1',title:'单位新闻'},
            {id:'2',title:'行业动态'},
            {id:'3',title:'文化建设'},
            {id:'4',title:'文明大展台'},
         ],
         tipsNew:[
            {id:'11',tips:'省计量院衡器与交通安全所派人赴山东泰安参加国家计量技术规范审定会',target:'省计量院衡器与交通安全所派人赴山东泰安参加国家计量',targetP:'全国公路专用计量器具计量技术委员会日前成立，将负责公路领域内计量技术规范制修订和...',
                toSpan:[
                    {id:'1',title:'省计量院衡器与交通安全所派人赴山东泰安参加国家计量技术规范审定会',target:'省计量院衡器与交通安全所派人赴山东泰安参...',},
                    {id:'2',title:'省计量院成功中标“安徽省高耗能行业能效对标指南研究”项目' ,target:'省计量院成功中标“安徽省高耗能行业能效对标...'},
                    {id:'3',title:'省计量院圆满完成2021年度废水类重点排污单位自动监测设备量值溯源工作',target:'省计量院圆满完成2021年度废水类重点排污单...'},
                    {id:'4',title:'省计量院2021年全力保障全省新冠疫情防控工作' ,target:'省计量院2021年全力保障全省新冠疫情防控工...'},
                    {id:'5',title:'省计量院圆满完成宿州市和铜陵市烟气自动监测设备量值溯源试点工作 ' ,target:'省计量院圆满完成宿州市和铜陵市烟气自动监...'},
                ]},
            {id:'12',tips:'公路专用计量器具计量技术委员会成立',target:'公路专用计量器具计量技术委员会成立', targetP:'全国公路专用计量器具计量技术委员会日前成立，将负责公路领域内计量技术规范制修订和... ',
                toSpan:[
                    {id:'1',title:'公路专用计量器具计量技术委员会成立' ,target:'公路专用计量器具计量技术委员会成立'},
                    {id:'2',title:'我国起草的首项振动在线校准国际标准即将发布' ,target:'我国起草的首项振动在线校准国际标准即将发...'},
                    {id:'3',title:'西安多名环保官员监测数据造假被警方带走', target:'西安多名环保官员监测数据造假被警方带走'},
                    {id:'4',title:'首届“互联网 检验检测认证”研讨会召开' ,target:'首届“互联网 检验检测认证”研讨会召开'},
                    {id:'5',title:'国家海洋计量站开展计量标准建立、使用和管理培训' ,target:'国家海洋计量站开展计量标准建立、使用和管理...'},
                ]},
            {id:'13',tips:'我院志愿者服务项目入选省直机关“最佳志愿者服务项目”',target:'我院志愿者服务项目入选省直机关“最佳志愿者服务项目”...',targetP:'2016年2月25日，根据《关于开展省直机关“最佳志愿服务项目、最佳志愿服务组织、最佳志愿者... ',
                toSpan:[
                    {id:'1',title:'我院志愿者服务项目入选省直机关“最佳志愿者服务项目”' ,target:'我院志愿者服务项目入选省直机关“最佳志愿者...'},
                ]},
         ],
         classChange:'1',
      }
   },
   components:{slideShow,},
   methods:{
        mouseover(id){
            if(id!=4){
                this.classChange = id
            }else{}
        },
        showOf(id){
            if(id == this.classChange){
                return 'display:block;'
            }else{return 'display:none;'}
        }
   }
}

</script>

<style lang='css' scoped> 
.news{ width:723px; height:274px; margin-top:14px;}
.dongtai{ width:415px; height:271px; border:1px solid #e7e7e7; border-top:1px solid #0151a1; float:right;}

.topNews{ width:389px; height:85px; border-bottom:1px dashed #e7e7e7; margin:10px 13px 0px;}
.topNews h1{ height:30px; line-height:30px; font-size:14px; text-align:center; font-family:"微软雅黑";}
.topNews h1 a{ color:#0151a1;}
.topNews p{ font-size:14px; color:#565656; margin:0px; padding:0px; line-height:20px;} 
.topNews p a{ color:#e30000;} 
.topNews p a:hover{ text-decoration:underline;}

.list2{ margin-top:5px;padding-left: 0px;}
.list2 li{ height:25px; line-height:25px; font-size:14px; margin:0px 13px; background:url(~@/assets/icon1.jpg) left center no-repeat; list-style: none;}
.list2 li a{ color:#565656; padding-left:10px;}  .list2 li a:hover{ color:#013366;}
.list2 li span{ float:right; color:#a9a7a7; font-size:12px;}

.title3{ height:35px; background:url(~@/assets/libg.jpg) repeat-x; font-family:"微软雅黑";}
.title3 h1{ height:35px; float:left; font-size:14px;margin-top: 0px;}
.title3 h1 a{ display:block; color:#252525; padding:0px 20px;margin-top: 7px;height: 28px;}
.title3 h1 a:hover{ background:#fff; color:#0151a1;}

</style>
