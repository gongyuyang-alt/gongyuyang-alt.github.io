# 网站信息更新指南

这个网站把经常变化的内容集中在少数几个文件中。通常不需要修改页面结构或样式。

## 1. 更新个人简介、研究方向与教育经历

编辑 `_data/profile.yml`：

- `role`、`affiliation`、`location`：当前身份与单位
- `headline`、`intro`：首页主标题和两句研究简介
- `availability`：是否开放实习、博士申请或合作
- `affiliation_sentence`、`mentors`：实验室与导师信息
- `research_themes`：三个主要研究方向
- `research_arc`：研究发展脉络
- `education`：学位、学校、时间和成绩

建议首页主标题只表达一个明确的研究问题，不要堆叠过多关键词。

## 2. 添加或更新论文

编辑 `_data/publications.yml`。复制一整条论文记录并放到文件顶部，然后更新：

- `title`、`short_title`
- `year`、`venue`、`status`
- `authors`：作者列表中请保留英文名 `Yuyang Gong`，网站会自动加粗
- `contribution`：用一句话说明论文解决了什么问题
- `tags`
- `paper_url`、`code_url`
- `selected: true`：同时显示在首页；`false`：只显示在 Publications 页面

Google Scholar 引用数会持续变化，因此网站没有手动写引用数，而是直接链接到 Scholar。

## 3. 更新头像和联系方式

- 替换 `images/profile.png` 可更新头像，建议使用清晰的竖版照片。
- 邮箱、Google Scholar、GitHub 等链接在 `_config.yml` 的 `author` 区域更新。
- 如果添加 LinkedIn，在 `_config.yml` 中填写 `author.linkedin` 的用户名。

## 4. 更新完整 CV

编辑 `_pages/cv.md`。研究经历与技能是手写内容；首页和论文数据会从上述两个数据文件自动读取。

如需提供 PDF 版 CV，把文件放到 `files/` 目录，并在导航或 CV 页面添加链接。

## 5. 调整导航与视觉样式

- 顶部导航：`_data/navigation.yml`
- 页面颜色、排版和卡片样式：`_sass/_research-site.scss`
- 网站标题、SEO 描述和社交链接：`_config.yml`

## 发布

这个仓库按 GitHub Pages 的标准结构组织。修改后提交并推送到默认分支，GitHub Pages 会重新构建网站。

