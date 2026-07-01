# WA_CHA_OLLAMA_ENTERPRISE_IMPORT_PACK_v1_EXECUTED

This release pointer describes the generated local Wa! AI import package.

## Files generated in the workspace

```text
WA_CHA_OLLAMA_ENTERPRISE_IMPORT_PACK_v1_EXECUTED.zip
WA_CHA_OLLAMA_ENTERPRISE_IMPORT_PACK_v1_EXECUTED.tar.gz
wa_ollama_import_pack_v1_EXECUTED_VALIDATION_REPORT.json
```

## Purpose

Package Wa! / Wa-cha! / RWAL / ABS / ATOMIC / 1CB / 1dfa1cb materials into a direct local import structure for Ollama and RAG-based retrieval.

## Install

```bash
unzip WA_CHA_OLLAMA_ENTERPRISE_IMPORT_PACK_v1_EXECUTED.zip
cd wa_ollama_import_pack_v1
bash scripts/install_wa_ollama.sh
```

## Manual Ollama build

```bash
ollama pull llama3.2
ollama create wa-cha-local -f 01_ollama/Modelfile
ollama run wa-cha-local
```

## Open WebUI Knowledge import

Create a Knowledge collection named:

```text
WA_EVERYTHING_RAG
```

Upload:

```text
02_rag_import_bundle/openwebui_knowledge_upload/
```

Attach the Knowledge collection to the `wa-cha-local` model.

## Validation

See `validation-report.md` and `CHECKSUMS.sha256.txt` in this folder.

## Limitation

The binary ZIP and TAR.GZ package files were generated and validated locally, but were not transferred through the connected GitHub tool because this session exposed only text-oriented GitHub file publishing actions.
