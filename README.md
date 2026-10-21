<p align="center">
  <img src="assets/logo.svg" alt="FederalRAG Logo" width="540">
</p>

# FederalRAG

High-throughput forensic document search and question-answering system specialized for scanned federal court records, depositions, and public disclosures.

## Architecture

* **Ingestion Pipeline**: Tesseract OCR and Poppler utilities extracting raw text, tables, and handwritten annotations from multi-page scanned PDF archives.
* **Vector Retrieval**: Chunking and embedding pipeline matching natural language queries against document indexes with ranked cosine similarity.
* **Synthesis Core**: Multi-provider LLM integration (Gemini, Groq) synthesizing structured answers with strict inline citations.
* **Explorer Interface**: React desktop environment featuring document navigation panels, snippet previews, and citation cross-referencing.

## Prerequisites

* Python 3.10+
* Node.js 18+ and npm
* Tesseract OCR (`sudo apt-get install tesseract-ocr`)
* Poppler utilities (`sudo apt-get install poppler-utils`)

## Configuration

Create a `.env` file in the project root:

```bash
MODEL_PROVIDER="gemini"
API_KEY="your_api_key_here"
GROQ_API_KEY="your_groq_api_key_here"
PORT="3000"
```

## Setup and Execution

### Automated Installation

```bash
chmod +x install.sh start.sh
./install.sh
```

### Launch Services

```bash
./start.sh
```

Access the web interface at `http://localhost:3000`.

## License

GPL-3.0-or-later. See LICENSE for details.
