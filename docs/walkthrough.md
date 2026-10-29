# 从新闻到工程记录和报告

**[简体中文](walkthrough.md) · [English](walkthrough.en.md) · [返回产品介绍](../README.md)**

本导览使用2026年10月29日实际网站的截图与导出成品。它展示当时的维护记录，不是实时官方项目状态。完整 AI 与程序分工见 [AI 协同工作流](ai-workflow.md)。

## 收集与核对

![真实新闻台账](../assets/news-workspace.png)

图中廉江倒送电新闻分别展示2026年10月26日的发布日期与10月22日的工程日期。程序读取正文并生成台账；配置 AI 时，后台预复核辅助判断实际事件、关联机组及节点。用户阅读核对后确认。[新闻原文](https://power.in-en.com/html/power-2480128.shtml)

## 确认后的项目状态

![真实项目台账](../assets/project-status.png)

图中陆丰机组处于不同工程阶段。确认新闻并不意味着一定更新阶段：系统需要判断节点是否真实发生，以及究竟涉及哪台机组。有有效更新时写入台账；进度可视化和核电地图从同一台账读取最新记录，人工维护同样联动。

## 进度展示与图片输出

![实际进度图工作台](../assets/progress-workspace.png)

用户可以筛选阶段、定位机组并下载完整图片。下图是网站绘制功能直接导出的全尺寸成品，保留原有图例和 Note 框，未用其他绘图程序重画。

![实际导出的进度图](../assets/progress-chart.png)

## 监管资料留存

![真实监管文件归档](../assets/regulatory-archive.png)

程序扫描官方栏目，AI 可辅助识别主体、类别和附件。用户可以查看官网正文、本地网页快照及已下载文件；按类型检索并管理回收站。官网失效不会自动删除已有健康存档。

## 选稿、编辑与实际报告

![真实报告工作台](../assets/report-workspace.png)

图中选中的文章为陆丰1号机组凝汽器安装报道。工作台展示英文摘要、FCD 后月数、照片与原文证据。AI 在配置 API 后参与校译和工程编辑，用户保留事实与输出的最终控制。[新闻原文](https://power.in-en.com/html/power-2480157.shtml)

![实际工程编辑版第一页](../assets/editorial-example-page-1.png)

[查看 PDF](../examples/lufeng-1-editorial-example.pdf) · [下载 Word](../examples/lufeng-1-editorial-example.docx)

以上为已保存生成内容经单篇导出得到的真实成品；仅公开副本的内部页眉署名和作者元数据做了展示用途调整，摘要与正文未经重写。原文新闻和照片权利归发布方。

最初使用虚构内容制作的[格式示例 PDF](../examples/engineering-report-demo.pdf)仍保留，与真实成品分开标注。公开材料不包含完整数据库、API 密钥或私有核心代码。
