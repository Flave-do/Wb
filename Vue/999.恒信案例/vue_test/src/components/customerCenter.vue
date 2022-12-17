<template>
    <div class="khzq">
        <div class="title_kh">
            <h1>客户专区</h1>
            <span><a href=''>更多</a></span>
        </div>
        <ul class="list_kh">

            <li v-for="p in twoBox" :key="p.id">
                <a href=''  :title='p.title'
                    target="_blank">{{p.target}}</a>
            </li>

        </ul>
    </div>

</template>

<script>
export default {
    name:'customerCenter',
   data() {
       return {
                 twoBox:[
                    {id:'1', 
                    title:'投诉、申诉制度',
                    target:"投诉、申诉制度",
                    },
                    {id:'2',
                    title:'送检注意事项',
                    target:"送检注意事项",
                    },
                    {id:'3',
                    title:'检测工作期限',
                    target:"检测工作期限",
                    },
                    {id:'4',
                        title:'检测工作流程',
                        target:"检测工作流程"
                    },
                    {id:'5',
                        title:'检测能力',
                        target:"检测能力",  
                    },
                    {id:'6',
                        title:'服务方式',
                        target:"服务方式",
                    },
                    {id:'7',
                        title:'付款方式',
                        target:"付款方式",
                    },
                    {id:'8',
                        title:'总体目标',
                        target:"总体目标",
                    },
                    {id:'9',
                        title:'服务承诺',
                        target:"服务承诺",
                    },
                    {id:"10",
                        title:"服务平台",
                        target:"服务平台",
                    },
                ],
      }
   },
}

</script>

<style lang='css' scoped> 

.khzq{ width:800px; height:97px; background:url(~@/assets/khzq.jpg) no-repeat;}
.title_kh{ width:72px; height:67px; border:1px solid #e7e7e7; background:#fff; font-family:"微软雅黑"; margin-left:5px; margin-top:15px; display:block; float:left;}
.title_kh h1{ width:72px; height:43px; line-height:43px; font-size:16px; color:#467bb0; text-align:center; border-bottom:1px solid #e7e7e7;}

.title_kh span{ display:block; width:72px; height:24px; line-height:24px; color:#565656; text-align:center;}
.list_kh{ width:635px; height:76px; float:left; margin-top:8px;padding-left: 0px;list-style:none;}
.list_kh li{ width:121px; height:31px; line-height:31px; background:url(~@/assets/li.jpg) no-repeat; float:left; margin-left:5px; margin-top:7px; text-align:center; font-size:14px;}
.list_kh li a{ color:#565656;}
.list_kh li a:hover{color:#0151a1;}
a {text-decoration:none; color:#666666;}
h1{margin: 0;padding: 0;}


</style>
