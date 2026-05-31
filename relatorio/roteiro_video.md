# Roteiro Vídeo — Assistente RAG Edifícios Verdes & Net Zero

Duração alvo: 5 a 7 minutos. Gravar tela + voz.

---

## 0:00 – 0:30 — Abertura

- Mostrar slide com título do projeto, nome da disciplina, integrantes.
- Fala: "Apresento o assistente técnico RAG para edifícios verdes e Net Zero de energia e água, desenvolvido para a Global Solution de Processamento de Linguagem Natural. O objetivo é permitir consultas em linguagem natural a documentos técnicos de certificações e manuais, sempre com citação da fonte."

## 0:30 – 1:15 — Problema e motivação

- Slide com bullets: certificações LEED, AQUA-HQE, Net Zero têm centenas de páginas; modelos generalistas conhecem só superficialmente; RAG resolve fundamentando em corpus auditável.
- Fala: "Modelos como Claude, GPT e Llama respondem em alto nível sobre LEED ou AQUA-HQE, mas erram nos requisitos específicos. O pipeline RAG conecta o modelo a uma base curada de documentos reais, tornando cada resposta verificável."

## 1:15 – 2:30 — Arquitetura

- Slide com diagrama do pipeline: corpus → limpeza → chunking → embeddings → ChromaDB → recuperação top-k → prompt + Ollama (qwen2.5:3b) → resposta com citações.
- Apontar para cada caixa enquanto fala.
- Fala: "Dez documentos técnicos passam por limpeza, são segmentados em chunks de 512 a 1024 tokens respeitando seções e créditos de certificação. Os chunks viram vetores pelo modelo multilingual-e5-base e são indexados em ChromaDB com persistência. Na consulta, a pergunta é vetorizada, recuperamos os top-3 chunks mais similares, montamos o prompt e a resposta sai pelo Llama-equivalente Qwen 2.5 3B rodando localmente via Ollama."

## 2:30 – 4:00 — Demonstração ao vivo

- Abrir o notebook `gs_rag_net_zero.ipynb`.
- Rolar até a célula da etapa 6 (RAG).
- Rodar uma pergunta nova ao vivo: "Como funciona um sistema de reaproveitamento de águas cinzas?"
- Mostrar a resposta gerada e a lista de fontes citadas (arquivo + categoria).
- Rodar segunda pergunta: "Quais critérios para dimensionar um sistema de captação de água pluvial?"
- Destacar que cada afirmação técnica vem com a marca [fonte, ano].

## 4:00 – 5:00 — Resultados da avaliação

- Abrir `saidas/tsne_categorias.png` e mostrar que as três categorias formam clusters distintos — evidência de que os embeddings discriminam bem o vocabulário técnico de cada gênero documental.
- Abrir `saidas/avaliacao_rag.md` rapidamente e comentar: dez perguntas avaliadas, quatro respostas tecnicamente sólidas, duas corretamente abstidas por ausência no corpus, quatro com problemas de citação atribuídos ao porte reduzido do modelo generativo.
- Abrir `saidas/comparacao_rag_vs_puro.md`: na pergunta sobre NBR 15575 o RAG admitiu a ausência da norma no corpus enquanto o modelo puro inventou seis coeficientes; na pergunta de água pluvial o RAG citou SABESP de forma rastreável enquanto o puro produziu lista genérica sem fonte.

## 5:00 – 6:00 — Conclusões e melhorias

- Slide com bullets:
  - RAG eleva rastreabilidade e honestidade quanto a lacunas
  - LLM de 3B parâmetros ainda é o gargalo em precisão de citações
  - Próximos passos: subir para modelo 7B–8B, adicionar re-ranker cross-encoder, busca híbrida BM25+denso, avaliação automática com RAGAS
- Fala: "O experimento confirma que o RAG melhora rastreabilidade e reduz alucinação em relação ao LLM puro, mas a qualidade final depende fortemente do porte do modelo generativo. Com um modelo de 8 bilhões de parâmetros e um cross-encoder de re-ranking, a precisão das citações tende a subir significativamente sem aumentar custo de infraestrutura."

## 6:00 – fim — Encerramento

- Slide final com agradecimento, repositório do projeto e contato.
- Fala: "O código completo, o corpus, o relatório crítico e as saídas estão no repositório do projeto. Obrigado."

---

## Checklist de gravação

- [ ] Fechar abas e notificações antes de iniciar
- [ ] Ollama rodando antes da demo
- [ ] Notebook já com kernel ativo (Idle)
- [ ] Microfone testado, sem ruído de fundo
- [ ] Resolução de tela 1080p ou superior
- [ ] OBS Studio ou Loom para gravação
- [ ] Subir vídeo em link não-listado no YouTube ou Google Drive
- [ ] Conferir duração final entre 5 e 7 minutos
