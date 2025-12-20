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

/* 新增：用于包裹视频的容器样式 */
.video-container {
    position: relative;
    width: 100%;
    /* 16:9 宽高比 (9 / 16 = 0.5625) */
    padding-bottom: 56.25%;
    height: 0;
    overflow: hidden;
    margin: 30px auto; /* 上下边距，居中 */
    border-radius: 15px; /* 与卡片圆角一致 */
    box-shadow: 0 6px 16px rgba(0,0,0,0.12); /* 与卡片阴影一致 */
    max-width: 800px; /* 设置最大宽度 */
}

.video-container iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: 0; /* 移除 iframe 默认边框 */
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

.preview-card {
    background-color: #fff3cd; /* 浅黄色背景表示预览版 */
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
    /* 占据两倍宽度 */
    grid-column: span 2;
    /* 在大屏幕上保持两倍宽度，在小屏幕上回退到单列 */
}

.preview-card:hover {
    background-color: #ffeaa7; /* 悬停时的颜色 */
    transform: translateY(-12px) scale(1.05); /* 稍微缩小缩放比例以适应更宽的卡片 */
    box-shadow: 0 20px 50px rgba(0,0,0,0.3);
    z-index: 10;
}

.preview-card::before {
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

.preview-card:hover::before {
    left: 100%;
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
    justify-content: center;
    align-items: center;
    text-align: center;
    min-height: 400px;
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

.preview-card .version-title {
    color: #856404; /* 预览版标题颜色 */
}

.version-card:hover .version-title {
    color: #007bff;
}

.preview-card:hover .version-title {
    color: #6f4d04; /* 预览版悬停标题颜色 */
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

/* 预览版的特殊按钮样式，更长一些 */
.preview-btn {
    min-width: 200px; /* 增加最小宽度 */
    padding: 16px 35px; /* 增加内边距使其更长 */
    background-color: #ffc107; /* 使用预览版的颜色 */
    font-size: 1.1em;
}

.preview-btn:hover {
    background-color: #e0a800; /* 预览版按钮悬停色 */
    transform: scale(1.15) translateY(-3px); /* 保持预览版的放大效果 */
    box-shadow: 0 10px 25px rgba(255, 193, 7, 0.6); /* 为黄色按钮定制阴影 */
}

/* 修复：为普通卡片内的按钮定义更明确的悬停效果 */
.version-card .download-btn:hover {
    background-color: #0056b3;
    transform: scale(1.2) translateY(-3px); /* 稍微加大放大比例，使其更明显 */
    box-shadow: 0 10px 25px rgba(0,123,255, 0.6);
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
    text-align: center;
    width: 100%;
}

.preview-card .update-summary h3 {
    color: #856404; /* 预览版摘要标题颜色 */
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
    .preview-card, .version-card {
        height: 380px;
    }
    /* 在中等屏幕上，预览卡可能太宽，强制为单列 */
    @media (max-width: 1200px) {
        .preview-card {
            grid-column: span 1; /* 回退到单列宽度 */
        }
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
    /* 在小屏幕上，预览卡也强制为单列 */
    .preview-card {
        grid-column: span 1;
    }
}

@media (max-width: 768px) {
    .download-container {
        grid-template-columns: 1fr;
        gap: 25px;
    }
    .preview-card, .version-card {
        height: auto;
        min-height: 320px;
        padding: 25px;
    }
    .preview-card:hover, .version-card:hover {
        transform: translateY(-5px) scale(1.05);
    }
}
</style>

<div class="app-description">
是一款最新颖的学习软件，拥有极简风格无需担心自己分心，最新版本为Beta 0.10.1预览版，完成了大部分功能，正在持续更新中……
</div>

<!-- 在应用描述之后，下载部分之前插入视频 -->
<div class="video-container">
    <iframe src="//player.bilibili.com/player.html?bvid=BV1QeZBYjE4W&autoplay=0" 
            scrolling="no" 
            border="0" 
            frameborder="no" 
            framespacing="0" 
            allowfullscreen="true">
    </iframe>
</div>

<div class="download-section">
<h1>下载</h1>

<div class="download-container">

<!-- 新增的预览版卡片 -->
<div class="preview-card">
    <h2 class="version-title">预览版：Beta 0.10.1</h2>
    <a href="https://wwbiu.lanzouv.com/iZvJY35jq7of" class="download-btn preview-btn">点击下载预览版</a>
    <div class="update-summary">
        <h3>版本更新摘要：</h3>
        <ul class="update-list">
            <li>完善了个性化主题</li>
            <li>添加了按键音效</li>
        </ul>
    </div>
</div>

<!-- 原有的其他版本卡片 -->
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
