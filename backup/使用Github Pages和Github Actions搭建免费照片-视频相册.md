 ### 项目介绍

`github-pages-gallery` 是一个开源项目，旨在帮助用户使用Github Pages和Github Actions免费搭建和托管照片/视频画廊。该项目提供了一个零成本的解决方案，无需编写代码，只需通过Github的Web界面即可完成所有操作。

### 项目快速启动

#### 1\. 创建Github账户

首先，访问 [Github注册页面](https://github.com/join) 创建并验证你的Github账户。

#### 2\. 使用模板创建仓库

点击 [使用此模板](https://github.com/gautamkrishnar/github-pages-gallery/generate) 按钮，输入仓库名称并创建新仓库。

#### 3\. 配置Github Pages

1.  进入新创建的仓库，点击 `Settings` 选项卡。
2.  在 `Code and automation` 部分，点击 `Pages` 选项。
3.  选择 `GitHub Actions` 作为Github Pages的源。

#### 4\. 编辑配置文件

在仓库中找到 `config.json` 文件，点击编辑按钮进行配置：

```
{
  "input": "/gallery",
  "output": "/build_output",
  "title": "Photo Gallery",
  "sort-albums-by": "title",
  "sort-media-by": "filename",
  "download-photos": "copy",
  "cleanup": true,
  "theme": "cards",
  "css": "/custom.css",
  "footer": "Copyright Text",
  "usage-stats": false
}

```

[官方说明文档](https://thumbsup.github.io/docs/3-configuration/misc-settings/)
#### 5\. 选择主题

你可以从以下主题中选择一个：

*   `mosaic`: [mosaic主题](https://thumbsup.github.io/demos/themes/mosaic/)
*   `cards`: [cards主题](https://thumbsup.github.io/demos/themes/cards/)
*   `classic`: [classic主题](https://thumbsup.github.io/demos/themes/classic/)
*   `flow`: [flow主题](https://thumbsup.github.io/demos/themes/flow/)

#### 6\. 上传照片/视频

将你的照片或视频上传到 `/gallery` 目录中。

#### 7\. 查看画廊

完成上述步骤后，你的画廊将自动部署到Github Pages，可以通过 `https://<你的用户名>.github.io/<仓库名>` 访问。

### 应用案例和最佳实践

#### 应用案例

*   **个人摄影师**：展示个人作品集。
*   **团队项目**：展示团队活动照片和视频。
*   **教育机构**：展示学生作品或课程项目。

#### 最佳实践

*   **定期更新**：定期上传新作品，保持画廊内容的新鲜度。
*   **优化图片**：使用适当的图片格式和尺寸，以提高加载速度。
*   **自定义主题**：根据个人喜好选择或自定义主题，提升用户体验。

### 典型生态项目

*   **Thumbsup**: 用于生成静态画廊页面的工具。
*   **Github Actions**: 提供持续集成和持续部署的平台。
*   **Github Pages**: 提供免费的静态页面托管服务。

通过结合这些工具，`github-pages-gallery` 提供了一个高效且免费的解决方案，帮助用户轻松搭建和管理照片/视频画廊。

[github-pages-galleryA zero dollar solution to host your photo/video gallery online using Github pages and GitHub Actions. No coding necessary. 项目地址:https://gitcode.com/gh\_mirrors/gi/github-pages-gallery](https://gitcode.com/gh_mirrors/gi/github-pages-gallery/?utm_source=artical_gitcode&index=bottom&type=card&webUrl "github-pages-gallery")

  

本文转自 [https://blog.csdn.net/gitblog\_00937/article/details/141989291](https://blog.csdn.net/gitblog_00937/article/details/141989291)，如有侵权，请联系删除。