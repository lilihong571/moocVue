<template>
    <div class="home-page">
        <!-- 使用组件 -->
        <headers></headers>
        <!-- <ul class="nav">
            <li>
                <img src="../assets/web.png"/>
                <span>前端开发</span>
            </li>
            <li>
                <img src="../assets/webservice.png"/>
                <span>后端开发</span>
            </li>
            <li>
                <img src="../assets/move.png"/>
                <span>移动开发</span>
            </li>
            <li>
                <img src="../assets/data.png"/>
                <span>数据库</span>
            </li>
            <li>
                <img src="../assets/bigdata.png"/>
                <span>云计算</span>
            </li>
        </ul> -->
        <ul class="nav">
            <li v-for="item in arrList">
                <!-- item是arrList里面的一项  src要接收变量，需要:-->
                <img v-bind:src='item.imgUrl'/>
                <span>{{item.name}}</span>
            </li>
        </ul>
        <!-- 引用组件 -->
        <!-- arrList传递到List组件中去 -->
        <List :arrList="array"></List>
        <!-- 页面跳转 -->
        <!-- <router-link :to="/detail"></router-link> -->
        <Footer></Footer>
    </div>
</template>
<script>
 //导入组件
import headers from '@/components/header/index.vue';
// 导入图片
import WebImg from '@/assets/web.png';
import Webservice from '@/assets/webservice.png';
import Move from '@/assets/move.png';
import Data from '@/assets/data.png';
import Bigdata from '@/assets/bigdata.png';
// 导入组件
import List from '@/components/lists/index.vue'
//导入图片
import Course1 from '@/assets/course1.jpg';
import Course2 from '@/assets/course2.jpg';
import Course3 from '@/assets/course3.jpg';
import Course4 from '@/assets/course4.jpg';
import Course5 from '@/assets/course5.jpg';
// 导入底部
import Footer from '@/components/footer/index.vue'
export default {
   data(){
       return{
           arrList:[],
           array:[],
       }
   },
    //初始化数据值
    mounted(){
        this.arrList = [{imgUrl:WebImg,name:'前端开发'},
           {imgUrl:Webservice,name:'后端开发'},
           {imgUrl:Move,name:'移动端开发'},
           {imgUrl:Data,name:'数据库'},
           {imgUrl:Bigdata,name:'云计算'}];
        this.array = [
            {imgUrl:Course1,title:'实例妙解Sed和Awk的秘密',des:'中级·330人在学'},
            {imgUrl:Course2,title:'Java定时任务调度工具详解之Quartz篇',des:'已学98% 中级·330人在学'},
            {imgUrl:Course3,title:'星级评分原理与实践',des:'中级·330人在学'},
            {imgUrl:Course4,title:'实例妙解Sed和Awk的秘密',des:'中级·330人在学'},
            {imgUrl:Course5,title:'PHP消息队列实践',des:'中级·330人在学'},
            {imgUrl:Course4,title:'实例妙解Sed和Awk的秘密',des:'中级·330人在学'},
            {imgUrl:Course5,title:'PHP消息队列实践',des:'中级·330人在学'}];
    },
   //注册组件
   components:{
       headers,List,Footer
   }
}
</script>
<style>
    .nav{
        height: 100px;
        padding-top: 44px;
        background: #f3f5f7;
        /* 多出来的上下滑动 */
        overflow-x: scroll;
        /* 左右滑动 */
        white-space: nowrap;
        font-size: 0;
    }
    .nav li{
        width: 88px;
        display: inline-block;
        font-size: 14px;
        text-align: center;
    }
    .nav li img{
        display: block;
        width: 32px;
        margin: 20px auto 12px;
    }
    
</style>