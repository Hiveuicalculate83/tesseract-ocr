<h1 align="center">Tesseract OCR Engine</h1>

<p align="center">
  Open source optical character recognition engine and command-line OCR program.
</p>

## 🔎 Overview

Tesseract is an open source OCR engine for recognizing text in images. The project provides both the `libtesseract` library and the `tesseract` command-line program.

Tesseract supports Unicode through UTF-8 and can recognize more than 100 languages when the appropriate trained data files are available. It supports common image input formats through Leptonica, including PNG, JPEG, and TIFF, and can produce several output formats such as plain text, hOCR, PDF, invisible-text-only PDF, TSV, ALTO, and PAGE.

Tesseract 4 introduced a neural network OCR engine based on LSTM line recognition. The legacy Tesseract 3 OCR engine is still supported through legacy OCR engine mode, provided compatible trained data files are used.

This project is an OCR engine and command-line tool. It does not include a graphical user interface.

## ✨ Key Capabilities

- OCR engine library: `libtesseract`
- Command-line OCR program: `tesseract`
- Unicode UTF-8 text support
- Recognition support for more than 100 languages with trained data
- Neural-network-based LSTM OCR engine
- Legacy OCR engine compatibility mode
- Input support for common image formats such as PNG, JPEG, and TIFF
- Output support for:
  - Plain text
  - hOCR
  - PDF
  - Invisible-text-only PDF
  - TSV
  - ALTO
  - PAGE
- C and C++ APIs for developers
- Trainable OCR support for additional languages

## 🧠 OCR Engines

Tesseract includes the modern LSTM-based OCR engine introduced in Tesseract 4. This engine is focused on line recognition and is the main OCR approach used by current Tesseract versions.

The legacy engine from Tesseract 3 remains available for compatibility. It can be selected with legacy OCR engine mode:

    --oem 0

Legacy mode requires trained data files that support the legacy engine, such as compatible files from the Tesseract tessdata resources.

## 🌍 Language and Data Support

Tesseract can recognize more than 100 languages when the required trained data files are installed. These trained data files define the language models used by the OCR engine.

Tesseract can also be trained to recognize additional languages. Training information is documented in the Tesseract documentation.

For OCR quality, the quality of the input image matters. In many cases, better preprocessing or a cleaner source image can improve recognition results.

## 🖼️ Input and Output

Tesseract uses the Leptonica library for opening input images. Supported input formats include widely used image types such as:

- PNG
- JPEG
- TIFF

Tesseract can produce multiple output formats depending on the intended workflow:

| Output format | Purpose |
| --- | --- |
| Plain text | Extracted text content |
| hOCR | HTML-based OCR layout output |
| PDF | Searchable document output |
| Invisible-text-only PDF | OCR text layer without visible text rendering |
| TSV | Tab-separated structured OCR data |
| ALTO | XML format used in document digitization workflows |
| PAGE | XML format for page layout and text recognition data |

## ▶️ Basic Usage

The general command-line form is:

    tesseract imagename outputbase [-l lang] [--oem ocrenginemode] [--psm pagesegmode] [configfiles...]

For command-line option details, use:

    tesseract --help

or consult the `tesseract` manual page where available.

## 🧩 Developer API

Developers can use `libtesseract` to integrate OCR capabilities into applications.

Available APIs include:

- C API
- C++ API

Bindings for other programming languages are documented separately in the Tesseract add-ons and wrapper documentation.

API documentation generated from source code is available through the Tesseract documentation site.

## 📚 Documentation

The Tesseract documentation covers installation, compilation, command-line usage, training, image quality guidance, input formats, APIs, planning notes, release notes, and frequently asked questions.

Useful documentation topics include:

- Installation guidance
- Building from source
- Command-line OCR usage
- Input format support
- Image quality improvement
- Training Tesseract
- Data files and language models
- API documentation
- Add-ons and wrappers
- FAQ and user support

## 🛠️ Dependencies

Tesseract uses the Leptonica library for opening input images. Leptonica support for related image libraries is commonly used for formats such as PNG and TIFF.

Mentioned dependencies and related libraries include:

| Component | Role |
| --- | --- |
| Leptonica | Image reading and image processing support |
| zlib | Compression support used by related image formats |
| libpng | PNG image support |
| libtiff | TIFF and multipage TIFF support |

## 👥 Who Uses Tesseract?

Tesseract is useful for workflows where text needs to be extracted from image-based content. Typical use cases include:

- Converting scanned pages into searchable text
- Extracting text from image files
- Creating searchable PDFs
- Processing document archives
- OCR experiments and research workflows
- Building applications that need embedded OCR through `libtesseract`
- Working with multilingual image text recognition

Because Tesseract provides both a command-line interface and a library API, it can be used directly by users or integrated into larger software systems.

## 🧾 Project Background

Tesseract was originally developed at Hewlett-Packard Laboratories Bristol UK and Hewlett-Packard Co, Greeley Colorado USA between 1985 and 1994. Additional work followed in later years, including a Windows port and C++ changes. HP open sourced Tesseract in 2005. From 2006 until August 2017, it was developed by Google.

Major version 5 is the current stable version line and began with release 5.0.0 on November 30, 2021.

## 🤝 Support

Before reporting an issue, review the project contribution guidelines and documentation. For questions, the recommended path is to read the documentation and FAQ first, then search existing discussions and past issues.

Support resources mentioned by the project include:

- Tesseract documentation
- FAQ
- User forum
- Developer forum
- Existing issue tracker discussions

Issues should be used for bugs rather than general support questions.

## 📄 License

The code is licensed under the Apache License, Version 2.0.

Tesseract also depends on other open source packages that may use different licenses. Leptonica is noted as using a BSD 2-clause style license.

## ❓ FAQ

### What is Tesseract?

Tesseract is an open source OCR engine. It provides a library, `libtesseract`, and a command-line program, `tesseract`, for recognizing text in images.

### Does Tesseract include a graphical interface?

No. Tesseract does not include a GUI application. It is an OCR engine and command-line tool.

### Which OCR engine does Tesseract use?

Current Tesseract versions include an LSTM-based OCR engine introduced in Tesseract 4. The legacy Tesseract 3 OCR engine is also available through legacy OCR engine mode when compatible trained data files are used.

### How many languages can Tesseract recognize?

Tesseract can recognize more than 100 languages with the appropriate trained data files.

### What image formats does Tesseract support?

Tesseract supports common image formats through Leptonica, including PNG, JPEG, and TIFF.

### Can Tesseract create searchable PDFs?

Yes. Tesseract supports PDF output, including invisible-text-only PDF output.

### Can developers embed Tesseract in applications?

Yes. Developers can use the C or C++ APIs provided by `libtesseract`. Wrappers for other languages are documented separately.

### Can Tesseract be trained for other languages?

Yes. Tesseract can be trained to recognize additional languages, with training guidance available in the Tesseract documentation.
