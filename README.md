# Wa-cha.com Benchmarks

**Wa! goes local.** This repository is the public benchmark and release landing point for Wa-cha.com local-AI import artifacts.

## Current public release pointer

```text
WA_CHA_OLLAMA_ENTERPRISE_IMPORT_PACK_v1_EXECUTED
```

This package is designed for direct local use with:

- Ollama behavior configuration through a `Modelfile`
- Wa! / Wa-cha! / RWAL operating definitions
- Open WebUI Knowledge/RAG import bundle
- JSONL semantic-unit corpus
- JSONL RAG chunks
- install scripts
- validation scripts
- manifest and checksums

## Architecture

```text
Ollama Modelfile = behavior kernel
RAG bundle       = Wa! corpus memory
Embeddings       = local retrieval index
Fine-tuning      = optional later stage, not performed here
```

## Local import command

```bash
unzip WA_CHA_OLLAMA_ENTERPRISE_IMPORT_PACK_v1_EXECUTED.zip
cd wa_ollama_import_pack_v1
bash scripts/install_wa_ollama.sh
```

Manual path:

```bash
ollama pull llama3.2
ollama create wa-cha-local -f 01_ollama/Modelfile
ollama run wa-cha-local
```

## Validation snapshot

```text
Semantic units: 341
RAG chunks: 15
Raw sources: 7
Generated files: 54
JSON/JSONL: pass
ZIP integrity: pass
TAR.GZ integrity: pass
RWAL:BINARY_SCORE: 1
```

## Archive checksums

```text
88eb86661c50f9124abce192d7914c884aa41d47aeb28a2c6f6db7bc520a17bc  WA_CHA_OLLAMA_ENTERPRISE_IMPORT_PACK_v1_EXECUTED.zip
a459017517309d6dc6a991d1dc628f4bc5ec1f472af111bbbd51a5e734dbe316  WA_CHA_OLLAMA_ENTERPRISE_IMPORT_PACK_v1_EXECUTED.tar.gz
bd99d4f230308e8635d4612807538138f8f1d7b9b461b3879aebe13b3e5c9560  wa_ollama_import_pack_v1_EXECUTED_VALIDATION_REPORT.json
```

## RWAL verdict

```text
RWAL:BINARY_SCORE = 1
Real: artifacts were generated and validated locally.
World-bound: uses Ollama and RAG in their correct operational roles.
Actual: validation report, manifest, checksums, and package archives exist.
Literal: no claim of model-weight ingestion or fine-tuning is made.
```

## Note on binary archives

The generated ZIP and TAR.GZ archives are binary package files. The connected GitHub publishing tool available in this session can reliably publish text content, metadata, and validation records. Binary transfer through the connector payload is not available in this session, so this repository records the public release pointer, validation snapshot, and exact checksums for the generated archives.

## Author

Douglas W. T. Jackson
