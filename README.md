# BORN ACCESSIBLE

This repository contains a minimal, **born-accessible EPUB** example.  
Designed for indie authors, publishers, and developers to reference **accessibility metadata, semantic structure, and alt text practices** in EPUB 3.3.

This sample was produced via **[Monoline](https://www.monoline.net)**, our preferred EPUB pipeline, to demonstrate proper accessibility compliance and clean structure.

---

## Repository Structure

```
born-accessible/
├── EPUB/
│ ├── content.opf # EPUB metadata, manifest, spine, accessibility info
│ ├── nav.xhtml # EPUB 3.3 navigation (TOC)
│ ├── css/style.css # Clean, semantic styling (Palatino body, sans-serif titles)
│ ├── images/
│ │ ├── cover.jpg # Cover image (1600×2500px)
│ │ └── logo.png # Monoline logo (transparent PNG)
│ └── text/
│ ├── whats-happening.xhtml
│ ├── born-accessible.xhtml
│ ├── onix-metadata.xhtml
│ ├── backlist.xhtml
│ ├── what-to-do.xhtml
│ ├── sample-files.xhtml
│ ├── bottom-line.xhtml
│ ├── title-page.xhtml
│ ├── copyright.xhtml
│ ├── cover.xhtml
│ └── toc.xhtml
├── META-INF/
│ └── container.xml
├── mimetype
├── born-accessible.epub # Validated, EAA-compliant EPUB 3.3 (CC0)
└── sample-onix.xml # ONIX 3.0 with accessibility metadata
```

* Each XHTML file is structured semantically.
* `<h1>` for chapter titles, `<h2>` for sub-sections.
* Lists, paragraphs, and images include proper markup and alt attributes.
* `content.opf` includes **born-accessible metadata** (`schema:accessibilityFeature`, `schema:accessibilitySummary`).

---

## How to use

1. Clone this repository:

```bash
git clone https://github.com/thornevald-publishing/sample-accessible-epub.git
cd sample-accessible-epub
```

2. Test locally using an EPUB reader (Calibre, Thorium, Adobe Digital Editions, etc.).

3. Optional: **Validate EPUB** using [EPUBCheck](https://github.com/w3c/epubcheck):

```bash
epubcheck born-accessible.epub
```
0 errors, 0 warnings (EPUB 3.3 + EAA compliant).  
Use the source files as a reference when building your own accessible EPUBs.

> Zip the folder contents into `sample.epub` before running EPUBCheck.

4. Reference the structure and metadata when creating your own accessible EPUBs.

---

- Each XHTML file uses **semantic markup**:  
  - `<h1>` for chapter titles  
  - Proper `<ul>`, `<p>`, and `<section role="doc-chapter">`  
  - Images include descriptive `alt` text  
- `content.opf` includes **born-accessible metadata**:  
  - `schema:accessibilityFeature` (structural navigation, TOC, alt text)  
  - `schema:accessibilitySummary`  
  - WCAG 2.1 AA conformance declaration  
- `sample-onix.xml` shows how to declare accessibility in distribution feeds  

## Why This Matters

The EU Accessibility Act (EAA) now requires all ebooks sold in the EU to meet accessibility standards.  
Older EPUBs without semantic structure or accessibility metadata may be rejected by retailers, libraries, or procurement systems.

This sample provides a practical baseline—not just theory—for indie authors to get compliant, right out of the box.

This repository is a Monoline-endorsed sample, showing the accessibility workflow we apply across production pipelines: semantic markup, alt text, clean CSS, and proper EPUB + ONIX metadata.

For more info: monoline.net

This sample is CC0 / Public Domain. Use it freely for testing, teaching, or reference.
