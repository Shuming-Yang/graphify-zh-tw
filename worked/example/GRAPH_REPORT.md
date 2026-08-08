# Graph Report - raw  (2026-08-08)

## Corpus Check
- cluster-only mode — file stats not available

## Summary
- 73 nodes · 134 edges · 5 communities
- Extraction: 100% EXTRACTED · 0% INFERRED · 0% AMBIGUOUS
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- parser.py
- storage.py
- api.py
- validator.py
- processor.py

## God Nodes (most connected - your core abstractions)
1. `load_index()` - 12 edges
2. `validate_document()` - 10 edges
3. `parse_file()` - 7 edges
4. `process_and_save()` - 7 edges
5. `_ensure_storage()` - 7 edges
6. `save_parsed()` - 7 edges
7. `save_processed()` - 7 edges
8. `delete_record()` - 7 edges
9. `parse_and_save()` - 6 edges
10. `enrich_document()` - 6 edges

## Surprising Connections (you probably didn't know these)
- `handle_get()` --calls--> `load_record()`  [EXTRACTED]
  api.py → storage.py
- `handle_delete()` --calls--> `delete_record()`  [EXTRACTED]
  api.py → storage.py
- `handle_search()` --calls--> `load_index()`  [EXTRACTED]
  api.py → storage.py
- `handle_enrich()` --calls--> `process_and_save()`  [EXTRACTED]
  api.py → processor.py
- `handle_enrich()` --calls--> `load_record()`  [EXTRACTED]
  api.py → storage.py

## Import Cycles
- None detected.

## Communities (5 total, 0 thin omitted)

### Community 0 - "parser.py"
Cohesion: 0.17
Nodes (15): handle_upload(), Accept a list of file paths, run the full pipeline on each, and return a…, batch_parse(), parse_and_save(), parse_file(), parse_json(), parse_markdown(), parse_plaintext() (+7 more)

### Community 1 - "storage.py"
Cohesion: 0.25
Nodes (14): delete_record(), _ensure_storage(), load_index(), load_record(), Storage module - persists documents to disk and maintains the search index. All…, Load the full document index from disk., Persist the index to disk., Write a parsed document to storage. Returns the assigned record ID. (+6 more)

### Community 2 - "api.py"
Cohesion: 0.15
Nodes (13): handle_delete(), handle_enrich(), handle_get(), handle_list(), handle_search(), API module - exposes the document pipeline over HTTP. Thin layer over parser,…, Fetch a document by ID and return it., Delete a document by ID. (+5 more)

### Community 3 - "validator.py"
Cohesion: 0.21
Nodes (13): Exception, check_format(), check_required_fields(), normalize_fields(), Validator module - checks that parsed documents meet schema requirements before…, Run all validation checks on a parsed document. Raises ValidationError on…, Raise if any required field is missing., Raise if the format is not in the allowed list. (+5 more)

### Community 4 - "processor.py"
Cohesion: 0.20
Nodes (13): enrich_document(), extract_keywords(), find_cross_references(), normalize_text(), process_and_save(), Processor module - transforms validated documents into enriched records ready…, Lowercase, strip extra whitespace, remove control characters., Pull non-stopword tokens from text, deduplicated. (+5 more)

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `validate_document()` connect `validator.py` to `parser.py`, `api.py`?**
  _High betweenness centrality (0.118) - this node is a cross-community bridge._
- **Why does `load_index()` connect `storage.py` to `api.py`, `processor.py`?**
  _High betweenness centrality (0.097) - this node is a cross-community bridge._
- **Why does `parse_file()` connect `parser.py` to `api.py`?**
  _High betweenness centrality (0.069) - this node is a cross-community bridge._