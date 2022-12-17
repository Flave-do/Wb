<template>
    <div class="search">
        <div class="logo"><a ><img src="~@/assets/logo.png"></a></div>
        <div class="searchbox">
            <input type="text" class="input1" value="请输入关键字" />
            <input type="image" class="btn" value=""  />
        </div>
    </div>

</template>

<script>
export default {
   data() {
        return {
        }
   },
}

</script>

<style lang='css' scoped> 
.search{
    width: 100%;
    height:90px;
    margin:0 auto;
}
.logo{ width:400px; height:90px; float:left;margin-left:100px;}
.searchbox{width: 200px; ;height:28px;float: right;margin-right:100px;margin-top:32px;background:url('~@/assets/input.jpg') no-repeat}
.input1{ width:30%px; height:25px; float:left; border:0px; padding-left:10px; background:none; color:#4a1515;margin-top: 1px;}
.btn{ width: 20px;height: 26px; margin-left:13px;background: url('~@/assets/btn.jpg');margin-top: 1px;}
.btn2{ float:left; margin-right:10px;}

</style>
