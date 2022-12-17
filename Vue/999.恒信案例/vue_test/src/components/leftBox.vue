<template>

   <div class="left_box">
            <div class="business_login">
                <ul>
                    <li><a href="/login" target="_top"><img src="~@/assets/service_platform_login.jpg"
                                style="width:254px;" /></a></li>
                </ul>
            </div>
            <div class="notice">
                <div class="title"><a href="http://www.ahhx.com/jlfw/list_67.aspx">&gt;&gt;更多</a>
                    <h1>通知公告</h1>
                </div>
                <div id="colee" style="overflow:hidden;height:280px;">
                    <div id="colee1">
                        <ul class="list">

                            <li v-for="p in notice" :key="p.id">
                                <a href="#" :title="p.title" target="_blank">{{p.target}}</a>
                                <br>
                                {{p.toDay}}
                            </li>

                        </ul>
                    </div>
                    <div id="colee2">
                        <ul class="list">

                            <li v-for="p in notice" :key="p.id">
                                <a href="#" :title="p.title"
                                    target="_blank">{{p.target}}</a><br>
                                {{p.toDay}}
                            </li>

                        </ul>
                    </div>
                </div>
            </div>
            <div class="flfg">
                <div class="title">
                    <h1>普法园地</h1>
                    <span><a href="">更多</a></span>
                </div>
                <div class="list3">

                    <li v-for="p in flfg" :key="p.id">
                        <span>{{p.toDay}}</span>
                        <a href="" :title="p.title" target="_blank">{{p.target}}</a>
                    </li>

                </div>

            </div>
   </div>

</template>
<script>
export default {
   name:'leftBox',
   data() {
    return {
        notice:[
            {id:'1',
                title:"安徽省计量科学研究院测厚激光位移传感器系统采购竞争性磋商公告",
                target:'安徽省计量科学研究院测厚激光位移传感器系统采购竞争性磋商...',
                toDay:'2021-11-24'},
            {id:'2',
                title:"安徽省计量科学研究院动力电池极片涂层均匀性在线计量测试系统开发相关设备采购竞争性磋商公告",
                target:"安徽省计量科学研究院动力电池极片涂层均匀性在线计量测试系...",
                toDay:"2021-11-24"
            },
            {id:'3',
                title:"电离辐射和电学计量标准实验室设备设施公开招标公告",
                target:"电离辐射和电学计量标准实验室设备设施公开招标公告",
                toDay:"2021-11-19"
            },
            {id:'4',
                title:"安徽省计量科学研究院宣传视频制作项目（第2包）成交结果公告",
                target:"安徽省计量科学研究院宣传视频制作项目（第2包）成交结果公告",
                toDay:'2021-11-17'
            },
            {id:'5',
                title:"焓差试验室一体化装置招标公告" ,
                target:'焓差试验室一体化装置招标公告',
                toDay:'2021-11-17'
            },
            {id:'6',
                title:"安徽省计量科学研究院宣传视频制作项目第2包（二次）竞争性磋商公告",
                target:"安徽省计量科学研究院宣传视频制作项目第2包（二次）竞争性磋商...",
                toDay:"2021-11-05"
            },
            {id:'7',
                title:"安徽省计量科学研究院测厚激光位移传感器系统采购竞争性磋商公告",
                target:"安徽省计量科学研究院测厚激光位移传感器系统采购竞争性磋商...",
                toDay:'2021-11-24'
            },
            {id:'8',
                title:"安徽省计量科学研究院动力电池极片涂层均匀性在线计量测试系统开发相关设备采购竞争性磋商公告",
                target:"安徽省计量科学研究院动力电池极片涂层均匀性在线计量测试系...",
                toDay:'2021-11-24'
            },
            {id:'9',
                title:"电离辐射和电学计量标准实验室设备设施公开招标公告",
                target:"电离辐射和电学计量标准实验室设备设施公开招标公告",
                toDay:'2021-11-19'
            },
            {id:'10',
                title:"安徽省计量科学研究院宣传视频制作项目（第2包）成交结果公告",
                target:"安徽省计量科学研究院宣传视频制作项目（第2包）成交结果公告",
                toDay:'2021-11-17'
            },
            {id:'11',
                title:"焓差试验室一体化装置招标公告",
                target:"焓差试验室一体化装置招标公告",
                toDay:'2021-11-17'
            },
            {id:'12',
                title:"安徽省计量科学研究院宣传视频制作项目第2包（二次）竞争性磋商公告",
                target:"安徽省计量科学研究院宣传视频制作项目第2包（二次）竞争性磋商...",
               toDAy:'2021-11-05'
            }

        ],
        flfg:[
            {id:'1',title:'《信访条例》和《安徽省信访条例》（新修订）',target:'《安徽省信访条例》' ,toDay:'2020-06-19'},
            {id:'2',title:'中华人民共和国监察法',target:'中华人民共和国监察法' ,toDay:'2018-09-10'},
            {id:'3',title:'中华人民共和国宪法',target:'中华人民共和国宪法' ,toDay:'2018-09-10'},
            {id:'4',title:'中华人民共和国行政许可法',target:'中华人民共和国行政许可法' ,toDay:'2017-08-07'},
            {id:'5',title:'中华人民共和国行政处罚法',target:'中华人民共和国行政处罚法' ,toDay:'2017-08-07'},
            {id:'6',title:'中华人民共和国行政强制法',target:'中华人民共和国行政强制法' ,toDay:'2017-08-07'},
            {id:'7',title:'中华人民共和国行政复议法',target:'中华人民共和国行政复议法' ,toDay:'2017-08-07'},
            {id:'8',title:'中华人民共和国行政诉讼法',target:'中华人民共和国行政诉讼法' ,toDay:'2017-08-07'},
        ]
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
.left_box{width:264px; display:block; overflow:hidden; float:left;}
.business_login{ width:262px; height:90px; background:#fff; margin:10px 0px;}
.business_login li{ margin-left:9px; margin-top:5px;}
ul{list-style: none;margin: 0;padding: 0;}
fieldset,img{border:0}
a {text-decoration:none; color:#666666;}
div{margin: 0;padding: 0;}

.list3{ margin-top:5px;}
.list3 li{ height:25px; line-height:25px; font-size:14px;background:url(~@/assets/icon1.jpg) left center no-repeat;}
.list3 li a{ color:#565656; padding-left:10px;}  .list3 li a:hover{ color:#013366;}
.list3 li span{ float:right; color:#a9a7a7; font-size:12px;}

.notice{ width:262px; height:321px; border:1px solid #dedede; background:#fff; border-top:1px solid #0151a1;}
.title{ height:35px; line-height:35px; background:url(~@/assets/t1.jpg) repeat-x;}
.title h1{ font-size:16px; color:#004b96; line-height:35px; float:left; font-family:"微软雅黑"; padding:0px 18px;font-weight: normal;margin: 0;}
.title a{ float:right; padding-right:7px; color:#565656;}
.list{ display:block; overflow:hidden; font-family:"宋体";}
.list li{line-height:25px; font-size:12px; color:#a9a7a7; background:url(~@/assets/icon1.jpg) left center no-repeat; margin:0px 10px; border-bottom:1px dashed #e7e7e7; padding-left:10px; }
.list li a{ color:#565656; font-size:14px;} .list li a:hover{ color:#0051a1;}
a:hover {text-decoration:none;color:#016bb2;}
</style>

