# Python Library Complex Table PDF Parsing Feasibility Study

Comparision of various mostly Python libraries and one Java library for parsing tables in PDF. Arguably in order from worst to best at parsing complex tables. Only Unstructured, LlamaParse, and Camelot can successfully handle complex tables with merged cells. LlamaParse usually has the best results but when LlamaParse fails, it fails spectacularly and there seems to be no way to adust in those cases. Camelot is the only library able to handle tables with merged cells without having to resort to ML models. Camelot also has more adjustable settings than the previous two ML based solutions.

## [pdfminer.six](https://pdfminersix.readthedocs.io/en/latest/)
Parse and group all objects from a PDF document into Python objects. Extract text, images (JPG, JBIG2 and Bitmaps), table-of-contents, tagged contents and more. Support for Chinese, Japanese and Korean CJK languages as well as vertical writing. Support for various font types (Type1, TrueType, Type3, and CID). Support for RC4 and AES encryption. Support for AcroForm interactive form extraction. No real table support.

## [PyMuPDF library](https://github.com/pymupdf/PyMuPDF)
Library that allows you to extract text, images, links from PDF files. Has interesting [extract key-value pairs](https://pymupdf.readthedocs.io/en/latest/recipes-text.html#how-to-extract-key-value-pairs-from-a-page) function. Able to write files. No real table support. 

## [pdfplumber](https://github.com/jsvine/pdfplumber)
Library for pdf processing that allows for extracting text, images, and tables from PDF files. Misses some tables.

## [Marker](https://github.com/VikParuchuri/marker)
Converts PDF to markdown including tables and code blocks accurately. Marker is a pipeline of deep learning models and requires Torch but works on GPU, CPU, or MPS. Can't handle merged cells in tables.

## [tabula-java](https://github.com/tabulapdf/tabula-java)
Java library specifically for extracting tables from PDF files. Doesn't seem to be getting updated lately. Provides two extraction methods: stream (for tables with clear lines) and lattice (for tables with cell boundaries).  Has to exclude merged cells to handle tables containing them correctly.

## [Unstructured](https://docs.unstructured.io/welcome)
Does not support Python 3.12 yet. Seems to need OCR for complex tables so misses a few numbers, but handles merged cells correctly.
https://github.com/sudarshan-koirala/youtube-stuffs/blob/main/data-cleaning/unstructured-table-extraction-from-pdf.ipynb

## [LlamaParse](https://www.llamaindex.ai/)
https://colab.research.google.com/drive/18KB9yXxDUeQGrEZEP1eCrXQ0dNB-Oazm?usp=sharing#scrollTo=aYIUKOJ_z0eY
The best so far. Handles merged cells correctly.

## Various LLMs in General
Free/Smaller models do not handle merged cells correctly while larger more expensive models can with the correct prompting.

## [pypdf_table_extraction (Camelot)](https://github.com/py-pdf/pypdf_table_extraction)
Provides two extraction methods: stream (for tables with clear lines) and lattice (for tables with cell boundaries). Handles merged cells correctly.


## To do -- Checkout 
[Extracting financial disclosure reports and police blotter narratives using OpenAI's Structured Output](https://gist.github.com/dannguyen/faaa56cebf30ad51108a9fe4f8db36d8)

[power of structured visual understanding using the VLM Run Platform](https://github.com/vlm-run/vlmrun-cookbook/tree/main)

[Mistral OCR. Specialized PDF Parsing](https://mistral.ai/en/news/mistral-ocr)



[Intelligent Document Processing 2.0 (IDP 2.0) Platform Powered by Large Language Models](https://github.com/Zipstack/unstract)
[marker-pdf Convert PDF to markdown with high speed and accuracy.](https://www.piwheels.org/project/marker-pdf/)
[Nougat a Visual Transformer model that performs OCR for processing scientific documents into a markup language](https://huggingface.co/docs/transformers/en/model_doc/nougat)
[PyPDF PDF library capable of splitting, merging, cropping, and transforming the pages of PDF files.](https://github.com/py-pdf/pypdf)
[ Data-Extraction-Code-Snippets ](https://github.com/NanoNets/Data-Extraction-Code-Snippets/blob/main/using_python_libraries_to_automate_data_entry.py)
https://nanonets.com/blog/extract-tables-from-pdf/
https://artifex.com/blog/table-recognition-extraction-from-pdfs-pymupdf-python
https://github.com/jsvine/pdfplumber
https://github.com/yigitkonur/swift-ocr-llm-powered-pdf-to-markdown