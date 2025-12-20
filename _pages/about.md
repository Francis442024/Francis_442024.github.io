---
permalink: /
title: "Student-Nightmare"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<style>
.app-description {
    margin: 20px 0;
}

.download-section h1 {
    margin-top: 30px;
    margin-bottom: 30px;
    font-size: 2em;
    color: #333;
}

.download-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 40px;
    padding: 30px 0;
    max-width: 100%;
}

.version-card {
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
    justify-content: center; /* 主轴居中 */
    align-items: center;     /* 交叉轴居中 */
    text-align: center;
    min-height: 400px;
}

/* 针对内容较多的卡片，确保内部元素也能居中 */
.version-card > * {
    align-self: center;
    max-width: 100%;
}

.version-card:hover {
    background-color: #e3f2fd;
    transform: translateY(-12px) scale(1.1);
    box-shadow: 0 20px 50px rgba(0,0,0,0.3);
    z-index: 10;
}

.version-card::before {
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

.version-card:hover::before {
    left: 100%;
}

.version-title {
    margin-top: 0;
    margin-bottom: 15px;
    color: #333;
    font-size: 1.5em;
    font-weight: bold;
    transition: color 0.3s ease;
    align-self: center;
    width: 100%;
    text-align: center;
}

.version-card:hover .version-title {
    color: #007bff;
}

.download-btn {
    display: inline-block;
    background-color: #007bff;
    color: white !important;
    text-decoration: none !important;
    padding: 14px 28px;
    border-radius: 12px;
    transition: all 0.3s ease;
    margin: 15px auto;
    font-weight: bold;
    box-shadow: 0 3px 8px rgba(0,123,255,0.4);
    min-width: 140px;
    text-align: center;
    border: none;
    cursor: pointer;
    font-size: 1em;
    text-decoration: none;
    align-self: center;
}

.download-btn:hover {
    background-color: #0056b3;
    transform: scale(1.15) translateY(-3px);
    box-shadow: 0 10px 25px rgba(0,123,255,0.6);
    color: white !important;
}

.update-summary {
    margin: 15px auto;
    padding-left: 15px;
    transition: transform 0.3s ease;
    flex-grow: 1;
    max-width: 100%;
    text-align: left;
    align-self: center;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.update-summary h3 {
    margin-top: 0;
    margin-bottom: 10px;
    color: #495057;
    font-size: 1.2em;
    font-weight: 600;
    text-align: center; /* 让"版本更新摘要："也居中 */
    width: 100%;
}

.update-list {
    margin: 0;
    padding-left: 20px;
    list-style-type: disc;
    text-align: left;
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.update-list li {
    margin: 6px 0;
    transition: color 0.3s ease;
    word-break: break-word;
}

.version-card:hover .update-list li {
    color: #495057;
}

/* 响应式调整 */
@media (max-width: 1400px) {
    .download-container {
        grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
        gap: 35px;
    }
    .version-card {
        height: 380px;
    }
}

@media (max-width: 1200px) {
    .download-container {
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 30px;
    }
    .version-card {
        height: 360px;
    }
}

@media (max-width: 992px) {
    .download-container {
        grid-template-columns: repeat(2, 1fr);
        gap: 30px;
    }
    .version-card {
        height: 360px;
    }
}

@media (max-width: 768px) {
    .download-container {
        grid-template-columns: 1fr;
        gap: 25px;
    }
    .version-card {
        height: auto;
        min-height: 320px;
        padding: 25px;
    }
    .version-card:hover {
        transform: translateY(-5px) scale(1.05);
    }
}
</style>

<div class="app-description">
是一款最新颖的学习软件，拥有极简风格无需担心自己分心，最新版本为Beta 0.10.0测试版，完成了大部分功能，正在持续更新中……
</div>

<div class="download-section">
<h1>下载</h1>

<div class="download-container">

<div class="version-card">
    <h2 class="version-title">版本：0.10.0</h2>
    <a href="https://wwwi.lanzouo.com/izi8c33snbhg" class="download-btn">点击下载</a>
    <div class="update-summary">
        <h3>版本更新摘要：</h3>
        <ul class="update-list">
            <li>全面统一设计语言</li>
            <li>增强文字清晰度</li>
            <li>添加了由李倬贤提供的游戏</li>
        </ul>
    </div>
</div>

<div class="version-card">
    <h2 class="version-title">版本：0.9.1</h2>
    <a href="https://wwwi.lanzouo.com/iVm1H2xi3sid" class="download-btn">点击下载</a>
    <div class="update-summary">
        <h3>版本更新摘要：</h3>
        <ul class="update-list">
            <li>将功能完善</li>
            <li>优化代码</li>
            <li>页面更加流畅</li>
            <li>支持触控屏以及鼠标直接点击</li>
        </ul>
    </div>
</div>

<div class="version-card">
    <h2 class="version-title">版本：0.8.0</h2>
    <a href="https://wwwi.lanzouo.com/iVm1H2xi3sid" class="download-btn">点击下载</a>
    <div class="update-summary">
        <h3>版本更新摘要：</h3>
        <ul class="update-list">
            <li>使用图形化界面</li>
            <li>增强用户使用体验</li>
            <li>重置设计语言</li>
        </ul>
    </div>
</div>

<div class="version-card">
    <h2 class="version-title">版本：0.7.1</h2>
    <p>点击<a href="https://wwwi.lanzouo.com/iHXVR2qqdnvc" class="download-btn">链接</a>下载，访问密码：ftqb （控制台最新版）</p>
    <div class="update-summary">
        <h3>版本更新摘要：</h3>
        <ul class="update-list">
            <li>优化文字界面</li>
            <li>优化使用体验</li>
            <li>增加文字助手</li>
        </ul>
    </div>
</div>

</div>
</div>
