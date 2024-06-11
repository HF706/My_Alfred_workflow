# PDF TOC Navigator

Frustrated by the lack of tools to quickly locate entries in PDF dictionaries, I developed PDF TOC Navigator. This tool indexes multiple PDFs, allowing you to search their tables of contents and instantly jump to the corresponding pages. To enhance usability, I've added features for editing and exporting table of contents, making it easier to manage and navigate your PDFs.

## Dependencies

* Command line tool - [pdftk-java](https://formulae.brew.sh/formula/pdftk-java)

Install pdftk via [Homebrew](https://brew.sh)

```
brew install pdftk-java
```

## Usage

### Index PDF files via the Universal Action.

First, index the PDF document using the universal action 'Indexing' to extract the table of contents information and store it in index files. You can also select multiple files and add them to a buffer, and then index all of these at once.

![image](https://github.com/HF706/My_Alfred_workflow/assets/34521475/083aebbf-af68-4a33-ac5f-36966ac1af59)

### Search TOC in multiple PDF files.

```
def keyword1 keyword2 ...
```

<img width="719" alt="image" src="https://github.com/HF706/My_Alfred_workflow/assets/34521475/23409974-5c7d-48d0-8b94-eb68dd7a2024">

### Search TOC in in a specific PDF file.

```
indexin PDF_Name
```

<img width="719" alt="image" src="https://github.com/HF706/My_Alfred_workflow/assets/34521475/9657e08c-b61b-4dbb-8bd3-28ef09afdef5">

### Export PDF Table of Contents


Use the universal action 'Export PDF Table of Contents'. It will show the TOC of the PDF in text view, adhering to the following format:

```
"content"\t"logical page number"

\t"content"\t"logical page number"
```

<img width="561" alt="image" src="https://github.com/HF706/My_Alfred_workflow/assets/34521475/51f31d06-999d-45d1-a3ef-056674a6cfbb">

Where:

* "content" represents the name of the entry in the table of contents.
* "Logical page number" refers to the page number as it would appear on the printed document, whereas “Physical page number” refers to the actual number of pages from the beginning of the PDF document. Page numbers before logical page 1 are represented using negative numbers.
* Use a tab ("\t") to separate the content from the page number, and add tabs at the beginning of each entry to indicate its level in the table of contents hierarchy. For instance, no tabs before a first-level entry, one tab before a second-level entry, and so forth.

<img width="669" alt="image" src="https://github.com/HF706/My_Alfred_workflow/assets/34521475/6e62c19d-c12b-41b5-98c8-2986def375ce">

### Add Table of Contents to PDF

* Edit the table of contents for your book in a text editor (using the format described above).
* Copy the edited text, and remember the physical page number that corresponds to logical page 1.
* Use the universal action 'Add Table of Contents to PDF', which parses the copied text. Then, enter the physical page number corresponding to logical page 1 in the input box. Wait a few seconds, and the table of contents will be successfully added to the PDF document.
