<template>
<div class="imgsNew">
            <div class="rollJpg">
                <ul :style="imgsEdge" @mouseover="end()" @mouseout="start()">
                    <li v-for="p in newTips" :key="p.id">
                        <a href='' :title='p.title' target="_blank"><img border="0" :src="p.imgSrc" /></a>
                        <div class="comt">{{p.comText}}</div>
                    </li>
                </ul>
            </div>
            <div class="tipsDiv">
                <a 
                  v-for="tip in newTips" :key="tip.id" 
                  :ref="'tip' +tip.id" 
                  class="tips" 
                  :style=styleSet(tip.id) 
                  @mouseover="mouseover(tip.id)" 
                  @mouseout="mouseout()"
                  >
                </a>
            </div>
        </div>

</template>

<script>
export default {
    name:'slideShow',
   data() {
        return {
            timer: null,// 初始定时器变量名为null,
            timerNumber:0,//用来调节图片滚动
            newTips:[
            {id:'0',
               title:'安徽省恒信检验检测有限公司注册地址位于蒙城县庄子大道东纬一路南侧江淮汽车零部件供应巢C' ,
               imgSrc:require("../assets/location.jpg") ,
               comText:'安徽省恒信检验检测有限公司...',
            },
            {id:'1',
               title:'公司年审会议中',
               imgSrc:require("../assets/new/1.jpg") ,
               comText:"公司年审会议中..."
            },
            {id:'2',
               title:'公司内部学习JJG 1033计量规范',
               imgSrc:require("../assets/new/2.jpg") ,
               comText:"公司内部组织学习JJG 1033计量规范..."
            },
            {id:'3',
               title:'许疃煤矿下井校准',
               imgSrc:require("../assets/new/3.jpg" ),
               comText:"公司开展许疃煤矿下井校准..."
            },
            {id:'4',
               title:'公司组织人员招聘',
               imgSrc:require("../assets/new/4.jpg") ,
               comText:"公司组织人员招聘..."
            },
            {id:'5',
               title:'洁净室检测中',
               imgSrc:require("../assets/new/5.jpg"),
               comText:"公司开展洁净室检验检测项目..."
            },
         ],
         imgsEdge:"margin-left: 0 px;",
         tipColor:0,
        }
   },

   methods:{
      styleSet(num){
         var backgroundColor = ''
         var lef = num * 30
         if (num ==this.tipColor){
            backgroundColor = 'red;'
         }else{
            backgroundColor = 'rgb(236, 236, 231);'
         }
         return "margin-left:"+ lef+"px;" + "backgroundColor:" + backgroundColor
      },

      //滚动轮播
      // start() {
      //    // 将定时器名字赋值到变量中
      //    this.timer = setInterval(() => {
      //       if (this.timerNumber <= 1812){
      //          this.imgsEdge = "margin-left: -"+ this.timerNumber +"px;"
      //          this.timerNumber += 1
      //          var tipTo = this.timerNumber%302
      //          if(tipTo==0){
      //             this.tipColor.unshift(parseInt(this.timerNumber/302))
      //          }else{}
      //       }else{
      //          this.timerNumber = 0
      //          this.tipColor.unshift('0')
      //          this.tipColor.splice(1)
      //       };
      //    }, 10);
      // },

      start() {
         // 将定时器名字赋值到变量中
         this.timer = setInterval(() => {
            if (this.timerNumber < 1510){
               this.timerNumber += 302
               this.imgsEdge = "margin-left: -"+ this.timerNumber +"px;"
               this.tipColor=parseInt(this.timerNumber/302)
            }else{
               this.timerNumber = 0
               this.imgsEdge = "margin-left: -"+ this.timerNumber +"px;"
               this.tipColor=0
            };
         }, 2500);
      },
      end() {
         clearInterval(this.timer);
         this.timer = null // 这里最好清除一下，回归默认值
         // 众所周知，定时器返回一个随机整数，用于表示定时器的编号，后面通过名字可以取消这个定时器的执行。
      },
      mouseover(id){
         this.end()
         this.imgsEdge = "margin-left:"+ -id*302 +"px;"
         this.timerNumber = id*302
         this.tipColor = id
      },
      mouseout(){
         this.start()
      },
   },

   mounted(){
      this.start()
   },

   beforeDestroy() {
      // js提供的clearInterval方法用来清除定时器
      clearInterval(this.timer);
   },
   // // beforeDestroy或destroyed钩子中都能去清除这个定时器
   // // destroyed() {
   // //   // clearInterval(this.timer);
   // // },


}

</script>

<style lang='css' scoped> 
.imgsNew{width:302px; border:1px solid #e7e7e7; height:271px; float:left;}
.imgsNew .tips{position: relative;width: 20px;height: 10px;float: left;background: rgb(236, 236, 231);margin-top: -56px;}
.imgsNew .tips:hover{background: rgb(235, 23, 23);}
.imgsNew .rollJpg{overflow:hidden; position:relative;}
.imgsNew .rollJpg ul{width:2114px; height:271px; padding-left: 0px;margin-top: 0px;}
.imgsNew .rollJpg li{float:left;position:relative;height:271px;list-style-type:none;}
.imgsNew .rollJpg li img{ width:302px; height:243px;}

.tipsDiv{margin-left: 90px;}

</style>
