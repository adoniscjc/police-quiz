[README_部署说明.txt](https://github.com/user-attachments/files/31778245/README_.txt)
2026公安基本级执法资格刷题系统 V7.1 PWA 一体版

【本版最重要变化】
- 已直接内置原223道母题 + Q224-Q1223扩展题1000道。
- 首次打开即有1223道题，无需再手动导入题库 JSON。
- 已内置 Q224-Q1223 对应 corrections 逐项解析数据。
- 保留题号跳转、顺序刷题、分类刷题、错题、收藏、笔记、模拟考试、学习统计、题库搜索等功能。
- 以后仍可以继续导入 Q1224 之后的新扩展题库。
- PWA 安装后可从手机桌面直接打开；首次成功缓存后可离线使用。

【安装前提】
PWA 必须通过 HTTPS 网站访问（或电脑 localhost 调试）。
不要直接通过微信 content:// 或手机 file:// 地址作为长期入口。

【推荐部署】
将本压缩包解压后，把以下文件/文件夹原样上传到 GitHub Pages、Cloudflare Pages、Netlify 或其他 HTTPS 静态网站：
index.html
manifest.webmanifest
service-worker.js
icons/

打开部署后的 HTTPS 地址后，在 Chrome/Edge 浏览器菜单中选择“安装应用”或“添加到主屏幕”。

【以后继续增加题目】
本版已经内置到 Q1223。以后生成的新扩展题库必须从 Q1224 连续编号。
程序中的“导入扩展题库”和“导入 corrections”功能仍然保留。

【学习数据】
答题记录、错题、收藏、笔记等仍保存在浏览器/PWA 本地存储中。
如果在同一网站地址上升级版本，原有学习数据通常可以继续保留。
