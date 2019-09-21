<template>
    <div class="c-header">
        <ul class="header-ul"> 
            <li>推荐</li>
            <li>课程</li>
            <li>实战</li>
            <li>职业路径</li>
            <li class="header-search"><img src="../../assets/search.png"/></li>
            <li class="header-history"><img src="../../assets/history.png"/></li>
        </ul>
    </div>
</template>
<style scoped>
    /* scoped表示写的这个样式仅用于这个组件  写的这个样式不会影响到其他页面 */
    .c-header{
        position: fixed;
        z-index: 3;
        top: 0;
        width: 375px;
        background-color: #ffffff;
        /* 阴影 */
        box-shadow: 0 2px 4px 0 rgba(0,0,0,0.10);
    }
    .header-ul{
        font-size: 0;
        /*解决inline-block引起的 上面也会有空格  */
    }
    .header-ul li{
        /* 一行展示  inline-block在有空格的相邻元素左右之间会产生4px的间隙   上面也会有空格*/
        display: inline-block;/*转换成行内元素 */
        /* 距离左边20px */
        padding-left: 20px;
        font-size: 16px;
        color: #71777d;
        height: 44px;
        line-height: 44px;
    }
    /* 两个图标定义成18px */
    .header-ul img{
        width: 18px;
    }
    .header-ul .header-search{
        padding-left: 60px;
    }
</style>