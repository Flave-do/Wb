<template>
  <div id="app">
      <handeTop/>
      <mainBox/>
      <Fte/>
  </div>
</template>

<script>
import handeTop from './components/handeTop'
import mainBox from './components/mainBox'
import Fte from './components/Fte'


export default {
  name: 'App',
  components: {handeTop,Fte,mainBox,  }
}
</script>

<style>
body{
	margin: auto;
	font-size:12px;
	color:#333;
	background:#fff; 
	font-family:Tahoma,Geneva,sans-serif,'宋体'; 
	min-width:1002px; 
	background:#FFFFFF url('~@/assets/1.jpg') repeat-x;;
	list-style: none;
	}
h1, h2, h3, h4, h5, h6 {
  font-weight: normal;
  }
  a{text-decoration:none};



</style>
