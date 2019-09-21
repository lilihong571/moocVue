<template>
    <div class='c-footer'>
        <ul class='footer-ul'>
            <li>
                <img src="../../assets/home.png"/>
                <span>首页</span>
            </li>
            <li>
                <img src="../../assets/sea.png"/>
                <span>发现</span>
            </li>
            <li>
                <img src="../../assets/download.png"/>
                <span>下载</span>
            </li>
            <li>
                <img src="../../assets/me.png"/>
                <span>我的</span>
            </li>
        </ul>
    </div>
</template>
<style scoped>
    .c-footer{
        width: 375px;
        position: fixed;
        bottom: 0;
        background: #fff;
        z-index: 3;
        border-top: 1px solid #F3F5F7;
    }
    .footer-ul{
        display: flex;
    }
    .footer-ul li {
        display: flex;
        height: 50px;
        flex: 1;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        font-size: 10px;
    }
    .footer-ul li img{
        width: 24px;
    }
</style>