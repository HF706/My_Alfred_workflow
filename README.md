# Search PDF Bookmarks.alfredworkflow

By using this workflow, users can easily search for information in multiple PDF documents and navigate to the corresponding page in a book.

```
def keyword1 keyword2 ...
```
![def](https://github.com/HF706/My_Alfred_workflow/assets/34521475/19a1f243-8fc1-484c-b6f9-24f1668c1288)

## Dependencies 依赖

* PDF Reader - [Skim](https://skim-app.sourceforge.io)(recommend, default), or any other PDF reader that supports URL schemes. But you should modify the default URL schemes in workflow.
* Command line tool - [pdftk-java](https://formulae.brew.sh/formula/pdftk-java)

Install pdftk via Homebrew

```
brew install pdftk-java
```

## Usage 用法

#### Indexing 建立索引

Index PDF file via the [Universal Action](https://www.alfredapp.com/help/features/universal-actions/).

![2](https://github.com/HF706/My_Alfred_workflow/assets/34521475/11870089-274a-4b99-929c-0d51f23fabf4)

You can also select multiple files and add them to a [buffer](https://www.alfredapp.com/help/features/file-search/#file-buffer), and then index all of these at once.

![3](https://github.com/HF706/My_Alfred_workflow/assets/34521475/f6407e68-b861-499e-ae71-4cf26b5dea73)


Search bookmarks in in a specific PDF file.

![indexin](https://github.com/HF706/My_Alfred_workflow/assets/34521475/2ff37565-c4f3-49f0-9b62-0d3160ec4c44)

### Search 搜索

Use the keyword followed by search terms.Press <kbd>↩</kbd> to open the page.

```
def keyword1 keyword2 ...
```

![4](https://github.com/HF706/My_Alfred_workflow/assets/34521475/e7d70396-2ace-4881-8554-699359938505)

List all indexed PDF files.

```
indexin
```

![5](https://github.com/HF706/My_Alfred_workflow/assets/34521475/dbe063f4-41fc-4042-9621-f3e1def364a5)

```
indexin PDF_Name
```

![6](https://github.com/HF706/My_Alfred_workflow/assets/34521475/6a4cd4a6-649a-40eb-aa42-38a054f812a8)

You can also search bookmark in in a specific PDF file.

```
keyword1 keyword2 ...
```

![7](https://github.com/HF706/My_Alfred_workflow/assets/34521475/cbebded9-735e-4cd3-80bc-2dbb093c3d21)
