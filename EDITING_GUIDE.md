# 网站信息更新指南

网站是一个单页主页：左侧是个人资料栏，右侧依次是 About Me、Research Interests、Publications、Education。
经常变化的内容集中在少数几个文件中，通常不需要修改页面结构或样式。

## 1. 个人信息、导师与教育经历

编辑 `_data/profile.yml`：

- `role`、`affiliation_short`：显示在左侧资料栏（例如 "Ph.D. student at NTU CCDS"）
- `affiliation`、`college`、`advisor`、`undergrad`：首页第一段自我介绍会自动引用
- `education`：Education 部分的条目，最新的放最上面；`note` 是可选的第二行

首页自我介绍和 Research Interests 的文字在 `_pages/about.md` 中直接修改。

## 2. 添加或更新论文

编辑 `_data/publications.yml`。复制一整条论文记录放到文件顶部，然后更新：

- `title`、`short_title`、`year`、`venue`
- `badge`：印在配图左上角的简短标签，例如 `CCS '26`、`Preprint`
- `authors`：请保留英文名 `Yuyang Gong`，网站会自动加粗；共同一作在名字后加 `<sup>&#42;</sup>`
- `paper_url`：标题和配图的跳转链接
- `links`：`{label, url}` 列表，显示为 "arXiv / Code / DOI"
- `to_appear: true`：在会议名后显示 "(to appear)"
- `selected: true`：以"配图 + 文字"的形式显示在 Publications；`false`：显示在 Other Publications 的简短列表中

### 论文配图

- 每篇 `selected: true` 的论文需要一张关键图，放在 `images/papers/`，并在 `image` 字段填文件名。
- 建议直接使用论文中的 overview / Figure 1，PNG 或 JPG，宽约 1200px，接近 16:9 的比例效果最好。
- 图片会完整显示在固定比例的框中（不会被裁掉），很宽的图可以只截取最有代表性的一块。
- 从 arXiv 源文件获取矢量图后，可用 `pdftoppm -r 200 -png -singlefile fig.pdf name` 转成 PNG。

完整论文列表与引用数以 Google Scholar 为准，网站只链接到 Scholar。

## 3. 头像和联系方式

- 头像：替换 `images/profile-oxford.jpg`（或修改 `_config.yml` 中 `author.avatar`），建议使用正方形照片，页面会显示为圆形。
- 邮箱、Google Scholar、GitHub 等链接在 `_config.yml` 的 `author` 区域更新；填写 `linkedin`、`twitter`、`orcid` 或 `cv` 后会自动出现在资料栏。
- `author.bio` 是名字下方的一句话标签。

## 4. 导航与视觉样式

- 顶部导航：`_data/navigation.yml`（链接到首页各个小节的锚点）
- 颜色、字号、论文框样式：`_sass/_homepage.scss`（文件顶部的 `$hp-*` 变量可整体换色）
- 网站标题、SEO 描述：`_config.yml`

## 本地预览与发布

```bash
bundle exec jekyll serve
```

修改后提交并推送到默认分支，GitHub Pages 会自动重新构建。若浏览器仍显示旧样式，把 `_config.yml` 中的 `asset_version` 改成新的值即可强制刷新 CSS。
