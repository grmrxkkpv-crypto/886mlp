MicTune MP3 音色工坊（网页版）

文件说明
- index.html：网页主程序，可直接用 Chrome / Edge / Safari 打开。
- manifest.webmanifest、sw.js、icon.svg：用于部署后支持离线缓存和添加到主屏幕/安装。

本地使用
1. 解压 ZIP。
2. 在电脑或 Android 手机上用最新版 Chrome / Edge 打开 index.html。
3. 选择 MP3，设置预设名称和映射强度。
4. 点击“分析 MP3 并生成预设”。
5. 下载生成的 .mttune.json，再在 MicTune 原有的音色配置导入功能中尝试导入。

部署为网站
将此文件夹中的所有文件一起上传到任意静态网站托管服务（例如 GitHub Pages、Cloudflare Pages 或 Netlify），确保 index.html 位于网站根目录。部署后可通过 HTTPS 网址访问；在支持 PWA 的浏览器中可以添加到主屏幕。不要只上传 index.html，否则离线缓存和安装元数据不会生效。

限制说明
- MP3 在浏览器本地解码和分析，不会上传到服务器。
- 生成物是基于 MP3 平均频谱映射得到的 8 段 EQ 参数预设（.mttune.json），不是 MP3 音频样本，也不是声线克隆模型。
- 该网页没有修改 MicTune APK，也没有为 MicTune 增加直接播放 MP3 音色的能力。
- 生成配置是否能被某个 MicTune 版本导入，仍需在对应版本中实际验证。
- 建议单个 MP3 文件小于 80 MB；如设备内存不足，请使用较短文件。
