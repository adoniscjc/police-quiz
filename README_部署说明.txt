2026公安基本级执法资格刷题系统 V7 PWA 使用说明

一、这个版本解决什么问题
1. 可以“添加到手机主屏幕”，像 App 一样启动。
2. 首次通过 HTTPS 打开并加载完成后，后续可离线使用。
3. 不再依赖微信 content:// 临时文件地址。
4. 保留原有刷题、错题、收藏、学习记录、扩展题库导入、题号跳转等功能。
5. 学习数据仍保存在当前浏览器/PWA 的本地存储中。

二、重要：不能直接双击 index.html 使用 PWA
PWA 的 Service Worker 必须运行在：
- HTTPS 网站；或
- localhost（电脑本地调试）

直接使用 file:// 打开 index.html 时，普通刷题页面可能能打开，但“安装到桌面”和离线缓存不会完整工作。

三、最简单免费部署方法：GitHub Pages
1. 新建一个 GitHub 仓库，例如 police-quiz。
2. 把本 ZIP 解压后的全部文件上传到仓库根目录：
   index.html
   manifest.webmanifest
   service-worker.js
   icons/
3. GitHub 仓库 → Settings → Pages。
4. Source 选择 Deploy from a branch。
5. Branch 选择 main / root，保存。
6. 等待几分钟后，用 GitHub Pages 给出的 HTTPS 地址在手机浏览器打开。
7. 浏览器菜单选择“添加到主屏幕”/“安装应用”；若浏览器支持，页面顶部也会出现“安装到桌面”按钮。

四、其他静态托管
Cloudflare Pages、Netlify、Vercel 等静态托管也都可以，原则是必须通过 HTTPS 访问。

五、安卓手机建议
优先使用 Chrome、Edge 等支持 PWA 安装的浏览器。
第一次打开后等待页面完全加载，再执行“添加到主屏幕”。
安装完成后以后直接点桌面图标进入，不再从微信打开 HTML 文件。

六、更新题库
仍可通过程序内部“导入扩展题库”功能导入 JSON。
如果你以后希望把 Q224-Q1223 的 1000 道题直接内置进 PWA，也可以再做一个“免导入一体版”。
