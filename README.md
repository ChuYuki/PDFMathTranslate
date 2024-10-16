# PDFMathTranslate

<p align="center">
  <!-- PyPI -->
  <a href="https://pypi.org/project/pdf2zh/">
    <img src="https://img.shields.io/pypi/v/pdf2zh"/>
  </a>
  <!-- License -->
  <a href="./LICENSE">
    <img src="https://img.shields.io/github/license/Byaidu/PDFMathTranslate"/>
  </a>
</p>

PDF scientific paper translation and bilingual comparison based on font rules and deep learning, preserving formula and figure layout.

![image](https://github.com/user-attachments/assets/57e1cde6-c647-4af8-8f8f-587a40050dde)

![image](https://github.com/user-attachments/assets/0e6d7e44-18cd-443a-8a84-db99edf2c268)

## Installation

```bash
pip install pdf2zh
```

## Usage

Execute the translation command in the command line to generate the translated document `example-zh.pdf` and the bilingual document `example-dual.pdf` in the current directory.

### Translate the entire document

```bash
pdf2zh example.pdf
```

### Translate part of the document

```bash
pdf2zh example.pdf -p 1-3,5
```

### Translate with the specified language

```bash
pdf2zh example.pdf -li en -lo ja
```

### Use regex to specify formula fonts and characters that need to be preserved

Hint: Starting from `\ufb00` is English style ligature.

```bash
pdf2zh BDA3.pdf -f "(CM[^RT].*|MS.*|XY.*|MT.*|BL.*|.*0700|.*0500|.*Italic)" -c "(\(|\||\)|\+|=|\d|[\u0080-\ufaff])"
```

## Acknowledgement

Document merging: [PyMuPDF](https://github.com/pymupdf/PyMuPDF)

Document parsing: [Pdfminer.six](https://github.com/pdfminer/pdfminer.six)

Multi-threaded translation: [MathTranslate](https://github.com/SUSYUSTC/MathTranslate)

Layout parsing: [LayoutParser](https://github.com/Layout-Parser/layout-parser)

## Star History

<a href="https://star-history.com/#Byaidu/PDFMathTranslate&Date">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=Byaidu/PDFMathTranslate&type=Date&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=Byaidu/PDFMathTranslate&type=Date" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=Byaidu/PDFMathTranslate&type=Date" />
 </picture>
</a>
