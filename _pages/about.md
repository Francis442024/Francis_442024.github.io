---
permalink: /
title: "Student-Nightmare"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<style>
.download-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 40px;
    padding: 30px;
    max-width: calc(4 * (min(320px + 80px, 100vw/4 + 80px)));
    margin: 0 auto;
}

.version-item {
    margin: 0;
}

.version-box {
    background-color: #f8f9fa;
    border-radius: 25px;
    padding: 30px;
    transition: all 0.5s cubic-bezier(0.25, 0.8, 0.25, 1);
    box-shadow: 0 6px 16px rgba(0,0,0,0.12);
    cursor: pointer;
    position: relative;
    overflow: hidden;
    transform: translateZ(0);
    backface-visibility: hidden;
    perspective: 1000px;
    height: 400px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    min-height: 400px;
}

.version-box:hover {
    background-color: #e3f2fd;
    transform: translateY(-12px) scale(1.1);
    box-shadow: 0 20px 50px rgba(0,0,0,0.3);
    z-index: 10;
}

.version-box::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(
        90deg,
        transparent,
        rgba(255,255,255,0.4),
        transparent
    );
    transition: left 1s;
}

.version-box:hover::before {
    left: 100%;
}

.version-box h2 {
    margin-top: 0;
    margin-bottom: 20px;
    color: #333;
    font-size: 1.5em;
    transition: color 0.3s ease;
    flex-shrink: 0;
    align-self: stretch;
}

.version-box:hover h2 {
    color: #007bff;
}

.download-link {
    display: inline-block;
    background-color: #007bff;
    color: white;
    text-decoration: none;
    padding: 14px 28px;
    border-radius: 12px;
    transition: all 0.3s ease;
    margin: 15px auto;
    font-weight: bold;
    box-shadow: 0 3px 8px rgba(0,123,255,0.4);
    flex-shrink: 0;
    min-width: 140px;
    text-align: center;
}

.download-link:hover {
    background-color: #0056b3;
    transform: scale(1.15) translateY(-3px);
    box-shadow: 0 10px 25px rgba(0,123,255,0.6);
    color: white;
}

.version-box ul {
    margin: 20px auto;
    padding-left: 20px;
    transition: transform 0.3s ease;
    flex-grow: 1;
    max-width: 100%;
    align-self: stretch;
}

.version-box:hover ul {
    transform: translateX(0);
}

.version-box li {
    margin: 10px 0;
    transition: color 0.3s ease;
    word-break: break-word;
    text-align: left;
}

.version-box:hover li {
    color: #495057;
}

@media (max-width: 1400px) {
    .download-container {
        grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
        gap: 35px;
    }
    .version-box {
        height: 380px;
    }
}

@media (max-width: 1200px) {
    .download-container {
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 30px;
    }
    .version-box {
        height: 360px;
    }
}

@media (max-width: 992px) {
    .download-container {
        grid-template-columns: repeat(2, 1fr);
        gap: 30px;
    }
    .version-box {
        height: 360px;
    }
}

@media (max-width: 768px) {
    .download-container {
        grid-template-columns: 1fr;
        gap: 25px;
        padding: 20px;
    }
    .version-box {
        height: auto;
        min-height: 320px;
        padding: 25px;
    }
    .version-box:hover {
        transform: translateY(-5px) scale(1.05);
    }
}
</style>

是一款最新颖的学习软件，拥有极简风格无需担心自己分心，最新版本为Beta 0.10.0测试版，完成了大部分功能，正在持续更新中……

# 下载

<div class="download-container">

<div class="version-item">
<div class="version-box">

## 版本：0.10.0
[点击下载](https://wwwi.lanzouo.com/izi8c33snbhg)

### 版本更新摘要：
1. 全面统一设计语言
2. 增强文字清晰度
3. 添加了由李倬贤提供的游戏

</div>
</div>

<div class="version-item">
<div class="version-box">

## 版本：0.9.1
[点击下载](https://wwwi.lanzouo.com/iVm1H2xi3sid)

### 版本更新摘要：
1. 将功能完善
2. 优化代码
3. 页面更加流畅
4. 支持触控屏以及鼠标直接点击

</div>
</div>

<div class="version-item">
<div class="version-box">

## 版本：0.8.0
[点击下载](https://wwwi.lanzouo.com/iVm1H2xi3sid)

### 版本更新摘要：
1. 使用图形化界面
2. 增强用户使用体验
3. 重置设计语言

</div>
</div>

<div class="version-item">
<div class="version-box">

## 版本：0.7.1
点击[链接](https://wwwi.lanzouo.com/iHXVR2qqdnvc)下载，访问密码：ftqb （控制台最新版）

### 版本更新摘要：
1. 优化文字界面
2. 优化使用体验
3. 增加文字助手

</div>
</div>

</div>
