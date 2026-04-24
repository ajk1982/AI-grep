# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.1] - 2026-04-24

### Fixed

- **macOS ripgrep install**: `setup` now falls back to `brew install ripgrep` when `apt-get` fails, fixing silent setup failures on macOS without a pre-installed `rg`
- **uv virtual environments**: `setup` now falls back to `uv pip install` when `pip` is unavailable in the active venv (uv omits pip by default), fixing silent optional-dependency failures
- **Office/PDF indexing**: `.docx`, `.xlsx`, `.xls`, and `.pdf` files are now correctly typed and their content extracted via `file_extract.py` during indexing; previously they were labelled `unknown` and read as raw bytes, causing silent extraction failures

## [1.0.0] - 2026-01-22

Initial public release of **AI-grep**.

### Features

- **Full-text search** with SQLite FTS5 and ripgrep
- **Incremental indexing** - only re-indexes changed files
- **Multi-format support** - plain text, markdown, source code, .docx, .xlsx, .pdf
- **AI/LLM optimized** - commands designed for minimal token usage

### Commands

**Setup & Maintenance:** setup, status, index, validate, config

**Search & Retrieval:** search, get, bundle, context, list

**Analysis & Discovery:** stats, timeline, tags, outline, toc

**Content Analysis:** related, duplicates, links, refs

**Multi-Source:** mount, sources, unmount

**Export & Integration:** export, clip, open, history

**Search Enhancements:** diff, grep-context, relevant
