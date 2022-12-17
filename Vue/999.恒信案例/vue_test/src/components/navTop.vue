<template>
    <div class="nav">
        <ul class="navmenu">
            <li>首页</li>
            <li v-for="p in navTopObj" :key="p.id" @mouseover="mouseOver(p.id)" @mouseleave="mouseLeave(p.id)">{{p.title}}
                    <div class='subNav' v-show="n===p.id">
                        <ul>
                            <li ><a v-for="(char, index) of p.subNavObj" :key="index" >{{char}}</a></li>
                        </ul>
                    </div>
            </li>
        </ul>    
    </div>

</template>

<script>

export default {
    name:'navTop',
    data() {
       return {
            navTopObj:[

                {id:'2','title':'信息公开',subNavObj:['本院简介','致辞','机构领导','组织机构','部门简介','工作理念','预决算公开']},
                {id:'3','title':'新闻中心',subNavObj:['单位新闻','行业新闻','图片新闻','文化建设',]},
                {id:'4','title':'资质能力',subNavObj:['法定计量机构授权','资质认定项目','授权或验收项目','CNAS认可项目','省级科技成果鉴定','节能量审核','固定资产投资项目评估']},
                {id:'5','title':'计量服务',subNavObj:['客户专区','通知公告','表格下载',]},
                {id:'6','title':'普法园地',subNavObj:['计量文化馆','政策法规','计量术语','民生计量','常见问题','普法专栏',]},
                {id:'7','title':'在线交流',subNavObj:['联系电话','意见反馈','监督举报','联系方式',]},

            ],
            n:0
      }
   },
   methods:{
        mouseOver(k){
            this.n=k
        },
        mouseLeave(k){
            this.n=0
        },

   },

}

</script>

<style lang='css' scoped> 
.nav{width:1002px; height:54px; margin:0 auto;}
.nav li{ position:relative;padding:0px 35px; height:54px; line-height:54px; float:left; text-align:center; font-family:"微软雅黑"; font-size:16px; background:right center no-repeat;z-index:99;display:block; line-height:54px; color:#0352a1;text-decoration:none;}
.navmenu li:hover{ color:#000;}

.navmenu .subNav { position:absolute; top:53px; left:0px; width:135px; background:#023A73; }
.navmenu .subNav ul { float:none; height:auto;padding-left: 0px }
.navmenu .subNav ul li { width:135px; height:36px; line-height:36px; float:left; height:auto; padding:0; background:none; font-family:\5b8b\4f53; font-size:12px; font-weight:100; text-align:center; }
.navmenu .subNav ul li a { display:block; color:#fff; }
.navmenu .subNav ul li a:hover { background:#fff; color:#0352a1; }

</style>
