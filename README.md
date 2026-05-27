# Zuan Gu 学术主页（重设计版）

现代化单页学术主页，重点展示期刊/会议论文，保留原站个人简介、经历与研究演示。

## 本地预览

```powershell
cd E:\AI_New\PIGS\guzuan-homepage
python -m http.server 8080
```

浏览器打开：<http://localhost:8080>

## 部署到 GitHub Pages

1. 将本目录内容复制到你的仓库 `guzuan.github.io`（或当前 Pages 仓库根目录）。
2. **从旧站复制 `images/` 目录**（头像、视频、LLM 图、favicon 等）：

   ```powershell
   # 若已 clone 旧仓库，示例：
   Copy-Item -Recurse "path\to\old-repo\images" "E:\AI_New\PIGS\guzuan-homepage\images"
   ```

   必需文件（与原站一致）：
   - `images/self.png`
   - `images/LLM.png`
   - `images/3dsgen.mp4`
   - `images/editanything.mp4`
   - `images/favicon-32x32.png`（可选）

3. 推送后 GitHub Pages 会自动更新：<https://gzaicebreak.github.io/guzuan.github.io/>

## 相对原站的改进

- **会议论文优先**展示，ZODS-RS 附带方法框架与实验结果图
- 期刊论文演示内嵌：`3dsgen.mp4` → Text-to-3D 论文；`LLM.png` → 人群仿真论文
- 已移除 Spline 背景与 Edit Anything 演示
- 修正 GitHub 链接为 `https://github.com/GzaIcebreak`
- 纯静态 HTML/CSS/JS，无需 Jekyll

## 自定义

- 论文条目：编辑 `index.html` 中 `.pub-list` 部分
- 配色与字体：修改 `css/styles.css` 顶部 `:root` 变量
