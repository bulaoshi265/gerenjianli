# 部署说明

这个文件夹已经是构建后的静态网页，可以直接部署到 GitHub Pages。

## 方式一：作为仓库根目录部署
1. 新建一个 GitHub 仓库。
2. 把这个文件夹里的所有文件（包括 `index.html` 和 `assets` 文件夹）上传到仓库根目录。
3. 打开仓库 Settings → Pages。
4. Source 选择 `Deploy from a branch`，分支选择 `main`，目录选择 `/ (root)`。
5. 保存后等待构建完成，即可通过 `https://<用户名>.github.io/<仓库名>/` 访问。

## 方式二：使用 /docs 目录部署
1. 把这个文件夹重命名为 `docs` 并放入仓库根目录。
2. Settings → Pages 的目录选择 `/docs`。
3. 保存后等待构建完成即可。

## 本地预览
直接在浏览器打开 `index.html` 即可预览，也可以使用任意静态服务器：
```bash
npx serve .
```

说明：本项目已在 `vite.config.js` 中设置 `base: './'`，因此使用相对路径，GitHub Pages 子路径部署无需额外配置。
