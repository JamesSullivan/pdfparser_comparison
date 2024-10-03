# Python Library Complex Table PDF Parsing Feasibility Study

Comparision of various Python libraries and one Java library for parsing tables in PDF. Arguably in order from worst to best at parsing complex tables. Only Unstructured, Camelot, and LlamaParse can successfully handle complex tables with merged cells. Camelot is the only library able to handle tables with merged cells without having to resort to ML models.

## [pdfminer.six](https://pdfminersix.readthedocs.io/en/latest/)
Parse and group all objects from a PDF document into Python objects. Extract text, images (JPG, JBIG2 and Bitmaps), table-of-contents, tagged contents and more. Support for Chinese, Japanese and Korean CJK languages as well as vertical writing. Support for various font types (Type1, TrueType, Type3, and CID). Support for RC4 and AES encryption. Support for AcroForm interactive form extraction. No real table support.

## [PyMuPDF library](https://github.com/pymupdf/PyMuPDF)
Library that allows you to extract text, images, links from PDF files. Has interesting [extract key-value pairs](https://pymupdf.readthedocs.io/en/latest/recipes-text.html#how-to-extract-key-value-pairs-from-a-page) function. Able to write files. No real table support. 

## [pdfplumber](https://github.com/jsvine/pdfplumber)
Library for pdf processing that allows for extracting text, images, and tables from PDF files. Misses some tables.

## [tabula-java](https://github.com/tabulapdf/tabula-java)
Java library specifically for extracting tables from PDF files. Doesn't seem to be getting updated lately. Misses some tables.

## [Marker](https://github.com/VikParuchuri/marker)
Converts PDF to markdown including tables and code blocks accurately. Marker is a pipeline of deep learning models and requires Torch but works on GPU, CPU, or MPS. Can't handle merged cells in tables.

## [Unstructured](https://docs.unstructured.io/welcome)
Does not support Python 3.12 yet. Seems to need OCR for complex tables so misses a few numbers, but handles merged cells correctly.
https://github.com/sudarshan-koirala/youtube-stuffs/blob/main/data-cleaning/unstructured-table-extraction-from-pdf.ipynb

## [Camelot](https://camelot-py.readthedocs.io/en/master/)
Provides two extraction methods: stream (for tables with clear lines) and lattice (for tables with cell boundaries). Handles merged cells correctly.

## [LlamaParse](https://www.llamaindex.ai/)
https://colab.research.google.com/drive/18KB9yXxDUeQGrEZEP1eCrXQ0dNB-Oazm?usp=sharing#scrollTo=aYIUKOJ_z0eY
The best so far. Handles merged cells correctly.

