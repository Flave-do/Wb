<template>
    <div class='hello'>
        <div class="department">
            <div class="title3">
                <h1 class="hovers" id="two1" @mouseover="mouseover(1)">
                    <a href='#' :style="[classify ==1 ? btnStyle:'none']">专业部门</a>
                </h1>
                <h1 id="two2" @mouseover="mouseover(2)">
                    <a href='#' :style="[classify ==2 ? btnStyle:'none']">资质能力</a>
                </h1>
            </div>

            <div class="con" id="con_two_1" :style="showOf(1,classify)">
                <template v-for="p in measuringRoom">
                    <h2 id="three1" :key="p.id+'11'" @mouseover="mouseoverThree(p.id)"  :class="[p.id==section ? blueClass:'rim']">
                        {{p.topText}}
                    </h2> 
                    <div class="coninfo" id="con_three_1" :key="p.id+'12'" :style="[p.id!=section ? tipStyle:'none']">
                        {{p.coninfo}}<a href="">[详细]</a>
                    </div>
                </template>
            </div>

            <div class="con" id="con_two_2" :style="showOf(2,classify)">
                <template v-for="p in accredit">
                    <h2 id="ten1"  @mouseover="mouseoverThree(p.id)" :key="p.id+'21' " :class="[p.id==section ? blueClass:'rim']">
                        {{p.topText}}
                    </h2>
                    <div class="coninfo" id="con_ten_1" :key="p.id+'22'" :style="[p.id!=section ? tipStyle:'none']"> 
                        {{p.coninfo}}<a href="">[详细]</a>
                    </div>
                </template>
            </div>
        </div>
    </div>

</template>

<script>
export default {
   data() {
        return {
            measuringRoom:[
                {id:'1',topText:'力学计量技术实验室',coninfo:'负责力学类检测工作，具体包括质量、力值、声学、振动、粘度、密度等项目，对检测结果和出具的报告、证书质量负责，并做好本部门测量设备的管理和维护保养工作，积极开展力学类检测技术的研究及产品的质量监督检验、委托检验、仲...',},
                {id:'2',topText:'长度计量技术实验室',coninfo:'负责几何量参数和光学参数方面与量值传递、溯源相关的计量器具检定、校准、检测（包括型式评价）及相关比对工作，对检测结果和出具的报告、证书质量负责；同时做好几何量计量和光学计量专业安徽省最高计量标准的维护、保养工...',},
                {id:'3',topText:'电学计量技术实验室',coninfo:'负责电磁类检测工作，对检测结果和出具的报告、证书质量负责，并做好本部门测量设备的管理和维护保养工作，积极开展电磁类检测技术的研究；完成领导交办的工作任务...',},
                {id:'4',topText:'计量器具强制检定',coninfo:'负责交通安全类检测工作，同时负责衡器类检测工作。具体包括汽车检测线设备、雷达测速仪等项目，对检测结果和出具的报告、证书质量负责，并做好本部门测量设备的管理和维护保养工作，积极开展交通安全类检测技术的研究；同时...',},
                {id:'5',topText:'热学计量技术实验室',coninfo:'热工计量技术研究所建立有安徽省地区的温度、湿度、压力和真空最高社会公用计量标准，热工所设有温湿度，压力，现场检测三个项目组。热工所长期以来一直坚持质量第一、客户至上、持续改进的宗旨，为客户提供准确、可靠的...',},
            ],
            accredit:[
                {id:'1',topText:'法定计量机构授权',coninfo:'安徽省计量科学研究院经国家质量监督检验检疫总局考核授权，是依法设置的法定计量检定机构。',},
                {id:'2',topText:'资质认定项目',coninfo:'国家气体流量仪表质量监督检验中心通过中国国家认证认可监督管理委员会的计量认证。安徽省计量器具质量监督检验中心、安徽省汽车产品质量监督检验站、安徽省能源计量和能效测试评价中心通过安徽省质量技术监督局的资质认定。',}
            ],
            classify:1,
            section:1,
            btnStyle:{
                background:' #fff',
                color: '#0151a1'
            },
            tipStyle:{
                display:'none',
            },
            blueClass:'blueClass'
       }
   },
   methods:{
        mouseover(id){
            if(id!=this.classify){
                this.classify = id
                this.section = 1
            }else{}
        },
        mouseoverThree(id){
            this.section = id
        },
        showOf(id,dataName){
            if(id == dataName){
                return 'display:block;'
            }else{return 'display:none;'}
        },
   }
}

</script>

<style lang='css' scoped> 
/* 专业部门 */
.department{ width:721px; height:251px;  border:1px solid #e7e7e7; margin-top:12px; background:#fff;}
.con{ width:697px; height:181px; margin:15px auto;}
.con h2{ width:16px; height:176px;padding:0px 15px; font-size:14px; color:#252525; line-height:14px; float:left; font-family:"微软雅黑"; padding-top:5px;}
.coninfo{ width:250px; height:171px; float:left; padding-left:10px; padding-top:10px;}
.coninfo{ font-size:14px; color:#565656; margin:0px; line-height:25px;} 
.coninfo a{ color:#e30000;}
.coninfo a:hover{ text-decoration:underline;}

.title3{ height:35px; background:url(~@/assets/libg.jpg) repeat-x; font-family:"微软雅黑";}
.title3 h1{ height:35px; float:left; font-size:14px;margin-top: 0px;}
.title3 h1 a{ display:block; color:#252525; padding:0px 20px;margin-top: 7px;height: 28px;}
.title3 h1 a:hover{ background:#fff; color:#0151a1;}

.list2{ margin-top:5px;}
.list2 li{ height:25px; line-height:25px; font-size:14px; margin:0px 13px; background:url(~@/assets/icon1.jpg) left center no-repeat;}
.list2 li a{ color:#565656; padding-left:10px;}  
.list2 li a:hover{ color:#013366;}
.list2 li span{ float:right; color:#a9a7a7; font-size:12px;}

.blueClass{background:url(~@/assets/lih.jpg) right no-repeat; color: #252525;border: 0px;}
.rim{border:1px solid #e7e7e7;}
</style>
