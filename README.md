# Assistente RAG — Edificios Verdes & Net Zero (Agua e Energia)

## Integrantes

| Nome | RM |
|------|----|
| Guilherme Gama | RM565293 |
| Igor Thiago Nakajima Vieira | RM563632 |

Global Solution — Processamento de Linguagem Natural, Chatbots & Virtual Agents.

Assistente tecnico que responde perguntas sobre **edificios verdes e Net Zero de energia e agua**,
sempre **citando a fonte**. Pipeline RAG 100% local: embeddings open-source + ChromaDB + LLM via Ollama.

## Stack

| Componente | Escolha | Motivo |
|-----------|---------|--------|
| Embedding | `intfloat/multilingual-e5-base` | retrieval assimetrico, forte em PT-BR tecnico, roda em CPU |
| Banco vetorial | ChromaDB (persistente) | filtro por metadados nativo, ideal p/ citacao |
| LLM local | Ollama `qwen2.5:3b` | pequeno porte, bom PT, sem API paga |

## Estrutura

```
gs-rag/
├── corpus/                 # >= 10 documentos (PDF/TXT/DOCX/HTML)  <- VOCE coloca aqui
├── metadata.csv            # metadados (copie de metadata_template.csv)
├── perguntas_teste.json    # 10 perguntas de avaliacao (valide com seu corpus)
├── requirements.txt
├── build_notebook.py       # gera o notebook
├── notebooks/
│   └── gs_rag_net_zero.ipynb   # ENTREGAVEL principal (8 etapas)
├── saidas/                 # gerado: relatorio chunking, avaliacao, comparacao, t-SNE
├── chroma_db/              # gerado: indice vetorial persistente
└── relatorio/
    └── relatorio_critico.md    # relatorio (>= 600 palavras) — preencher
```

## Passo a passo

1. **Dependencias**
   ```bash
   py -3 -m pip install -r requirements.txt
   ```
2. **Ollama** — instale (https://ollama.com) e baixe o modelo:
   ```bash
   ollama pull qwen2.5:3b
   ```
3. **Corpus** — coloque >= 10 documentos em `corpus/` (>= 3 categorias: certificacao/norma,
   relatorio tecnico, manual de tecnologia).
4. **Metadados** — copie `metadata_template.csv` para `metadata.csv` e edite com SEUS arquivos.
   A coluna `arquivo` deve bater exatamente com o nome na pasta `corpus/`.
5. **Rode** o notebook `notebooks/gs_rag_net_zero.ipynb` celula a celula.
6. **Avaliacao** — confira `saidas/avaliacao_rag.md` e marque manualmente se cada info confere
   com a fonte citada. `saidas/comparacao_rag_vs_puro.md` traz RAG vs LLM puro.
7. **Relatorio** — escreva `relatorio/relatorio_critico.md` (>= 600 palavras) usando os insumos
   impressos na Secao 8 do notebook.

## Mapa etapas do enunciado -> notebook

1 Planejamento · 2 Corpus · 3 Limpeza · 4 Chunking · 5 Embeddings+ChromaDB ·
6 Pipeline RAG (Ollama) · 7 Avaliacao (10 perguntas + RAG vs puro) · 8 t-SNE + relatorio.

## Regenerar o notebook

```bash
py -3 build_notebook.py
```
