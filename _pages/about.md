<div class="main-content">
    <div class="app-description">
        <p>是一款最新颖的学习软件，拥有极简风格无需担心自己分心，最新版本为Beta 0.10.0测试版，完成了大部分功能，正在持续更新中……</p>
    </div>

    <h1>下载</h1>

    <div class="download-container">
        <div class="version-item">
            <div class="version-box">
                <h2>版本：0.10.0</h2>
                <a href="https://wwwi.lanzouo.com/izi8c33snbhg" class="download-link">点击下载</a>
                <h3>版本更新摘要：</h3>
                <ul>
                    <li>全面统一设计语言</li>
                    <li>增强文字清晰度</li>
                    <li>添加了由李倬贤提供的游戏</li>
                </ul>
            </div>
        </div>

        <div class="version-item">
            <div class="version-box">
                <h2>版本：0.9.1</h2>
                <a href="https://wwwi.lanzouo.com/iVm1H2xi3sid" class="download-link">点击下载</a>
                <h3>版本更新摘要：</h3>
                <ul>
                    <li>将功能完善</li>
                    <li>优化代码</li>
                    <li>页面更加流畅</li>
                    <li>支持触控屏以及鼠标直接点击</li>
                </ul>
            </div>
        </div>

        <div class="version-item">
            <div class="version-box">
                <h2>版本：0.8.0</h2>
                <a href="https://wwwi.lanzouo.com/iVm1H2xi3sid" class="download-link">点击下载</a>
                <h3>版本更新摘要：</h3>
                <ul>
                    <li>使用图形化界面</li>
                    <li>增强用户使用体验</li>
                    <li>重置设计语言</li>
                </ul>
            </div>
        </div>

        <div class="version-item">
            <div class="version-box">
                <h2>版本：0.7.1</h2>
                <p>点击<a href="https://wwwi.lanzouo.com/iHXVR2qqdnvc" class="download-link">链接</a>下载，访问密码：ftqb （控制台最新版）</p>
                <h3>版本更新摘要：</h3>
                <ul>
                    <li>优化文字界面</li>
                    <li>优化使用体验</li>
                    <li>增加文字助手</li>
                </ul>
            </div>
        </div>
    </div>
</div>

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
    justify-content: center; /* 内容居中对齐 */
    align-items: center; /* 水平居中 */
    text-align: center; /* 文字居中 */
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
    align-self: stretch; /* 让标题占满全宽以保持居中对齐 */
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
    margin: 15px auto; /* 上下边距15px，左右自动居中 */
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
    margin: 20px auto; /* 左右自动居中 */
    padding-left: 20px;
    transition: transform 0.3s ease;
    flex-grow: 1;
    max-width: 100%; /* 限制最大宽度 */
    align-self: stretch;
}

.version-box:hover ul {
    transform: translateX(0); /* 居中状态下不需要水平移动 */
}

.version-box li {
    margin: 10px 0;
    transition: color 0.3s ease;
    word-break: break-word;
    text-align: left; /* 列表项文字左对齐，更易读 */
}

.version-box:hover li {
    color: #495057;
}

/* 调整在不同屏幕下的表现 */
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

