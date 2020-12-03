<template>
    <div class="app g-bd5 f-cb">
        <div class="g-sd51 left">
            <ul class="list">
                <li class="list-item">
                    <router-link to="/">> 首页</router-link>
                </li>
                <li class="list-item">
                    <router-link to="/about/us">> 关于我们</router-link>
                </li>
                <li class="list-item">
                    <a href="https://github.com/Hacker-Linner/k8s-micro-ssr" target="_blank">Demo ：k8s-micro-ssr</a>
                </li>
            </ul>
            <h3>我是基础的页面聚合渲染微服务，包含公共导航 —— <a href="https://github.com/Hacker-Linner/k8s-micro-ssr-common" target="_blank">k8s-micro-ssr-common</a></h3>
            
            <ul class="list">
                <li class="list-item">
                    <a href="https://k8seggjs.hacker-linner.com/" target="_blank">点我 -> 一起云原生！</a>
                </li>
                <li class="list-item">
                    <a href="https://github.com/fmfe/genesis" target="_blank">Thanks -> Genesis </a>
                </li>
            </ul>
        </div>
        <div class="g-mn5 middle">
            <div class="g-mn5c">
                <router-view />
            </div>
        </div>
        <div class="g-sd52 right">
            <h3>Cloud Native!（云原生） — 探索基于 Kubernetes，支持 SSR 和 CSR 渲染的微服务解决方案</h3>
        </div>
    </div>
</template>
<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
    name: 'app',
    data() {
        return {
            installed: false,
            show: true
        };
    },
    mounted() {
        this.installed = true;
    },
    methods: {
        close() {
            this.show = false;
        }
    }
});
</script>
<style lang="less">
html,
body {
    width: 100%;
    height: 100%;
    margin: 0;
    padding: 0;
}
body {
    overscroll-behavior-y: none;
}

/* 三列中间自适应布局 */
.g-bd5{margin:0 0 10px;}
.g-sd51,.g-sd52{position:relative;float:left;width:230px;margin:0 -230px 0 0;}
.g-sd52{float:right;width:190px;margin:0 0 0 -190px;}
.g-mn5{float:left;width:100%;}
.g-mn5c{margin:0 200px 0 240px;}
</style>
<style lang="less" scoped>
.title {
    text-align: center;
}
.app {
    position: relative;
    box-sizing: border-box;
    height: 100%;

    > div{
        height: 100%;
    }
}
.left {
    background: #e7f4e4;
}
.middle {
    background: #fff;
}
.right {
    background: #e7f4e4;
}
.list {
    margin: 0;
    padding: 15px;
}
.list-item {
    line-height: 38px;
    list-style: none;
}
</style>
