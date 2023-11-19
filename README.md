# Search PDF Content 使用方法

## 需要安装的依赖

确保计算机安装了 Python3 和 命令行工具 pdftk，
pdftk 可以通过 Homebrew 安装
```
brew install pdftk-java
```
## 使用方法

搜索 PDF 文件，并使用 Universal Actions 建立书签索引，索引默认位置在 Workflow 的工作目录 `./bookmark/` 中，建议修改储存路径，如果储存在工作目录，那么下次更新 Workflow 时会被删除。

<img width="1200" alt="image" src="https://github.com/HF706/My_Alfred_workflow/assets/34521475/a33b27a2-6843-4f3b-aeb6-262d5642e2d2">


### 索引
<img width="764" alt="image" src="https://github.com/HF706/My_Alfred_workflow/assets/34521475/b98ffe34-1e20-4828-af55-e812c62c7be1">

### 确认正文页（书籍第一页对应的 PDF 文件页码）

自动检测正文页，如果不为空，说明 PDF 文件中包含了正文页页码的信息，确认即可，如果不是，可修改。

<img width="766" alt="image" src="https://github.com/HF706/My_Alfred_workflow/assets/34521475/ad21197f-8b9d-4d83-9835-0d7fcb8e6aca">

### 搜索

支持一般搜索，支持中文分词；支持在指定文件中搜索；支持正则表达式搜索。默认使用 Skim 打开 PDF 指定页，可自行修改 URL scheme ，理论上支持所有 PDF 阅读器，即便没有提供 URL scheme 也可以通过 Keyboard Maestro 的 URL scheme 打开（后续更新教程）。

#### 搜索目录内容，可输入多个关键词，空格分隔。

![b45800cc66ea7c5af3c41b9b5f642fe916bda466](https://github.com/HF706/My_Alfred_workflow/assets/34521475/8a2c4105-e7ea-4600-b198-2894c07aeaf8)

#### 在指定 PDF 文件中搜索目录内容，空格分隔多个关键词。

![Screen Recording 2023-11-15 at 09 22 39](https://github.com/HF706/My_Alfred_workflow/assets/34521475/d0d61e37-c22b-4f95-a83c-2e8d256d22f1)

#### 支持正则表达式搜索目录内容。

![2784e376f009ce22355e360118c438b23841c3d9](https://github.com/HF706/My_Alfred_workflow/assets/34521475/160a769e-6a6a-48fd-ab49-6ffd09d90507)

# TODO

- [ ] 使用 tag 给索引文件加上标签，运行用户使用 tag # 进一步缩小文件搜索范围，实现在符合 tag 的文件中搜索书签
- [ ] 支持“真” 中文分词
- [ ] 整合我的另一个 Workflow - PDF Toolbox ，使得添加书签和修改书签变得更容易
- [ ] 更加详细的教程
