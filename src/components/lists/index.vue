<template>
        <ul class="c-course">
            <!-- router-link最后会解译成a标签 -->
            <router-link to="/detail">
                <li v-for="item in arrList">
                    <img :src="item.imgUrl"/>
                    <h1>{{item.title}}</h1>
                    <p>{{item.des}}</p>
                </li>
            </router-link>
        </ul>
</template>
<script>
export default {
    // 用于接收从父组件传过来的数据
    props:{
         arrList:Array,
    },
}
</script>
<style scoped>
    .c-course{
        padding: 24px 0;
        background-color: #fff;
    }
    .c-course li{
        position: relative;
        width: 335px;
        height: 72px;
        margin: 0 auto 24px;
    }
    .c-course li h1{
        padding-left: 124px;
        color: #2B333B;
        font-size: 15px;
    }
    .c-course li p{
        font-size: 12px;
        padding: 8px 0 0 124px;
        color: #71777D;
    }
    .c-course li img{
        width: 108px;
        position: absolute;
        border-radius: 5px;
    }
</style>