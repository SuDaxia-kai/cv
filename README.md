# 苏浩楷 · 在线简历

网站：https://sudaxia-kai.github.io/cv/

GitHub Pages 从 `main` 分支根目录发布。提交更新后会自动重新部署。

## 更新简历

在父目录重新生成 `main.pdf` 后，在本目录执行：

```sh
cp ../main.pdf resume.pdf
pdftoppm -scale-to 2000 -png resume.pdf resume
```

检查所有页面；若页数变化，同步调整 `index.html` 中的页面图片和页码，并移除不再使用的旧预览图。之后仅提交需要发布的文件：

```sh
git add index.html resume.pdf resume-*.png
git commit -m "Update resume"
git push origin main
```

本仓库仅包含公开简历、预览图片和网页，不包含 LaTeX 源码及本地笔记。
