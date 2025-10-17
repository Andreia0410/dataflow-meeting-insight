# dataflow-meeting-insight
Automated workflow to transcribe meetings, extract insights, and analyze SQL queries for business problem-solving.

# 📊 dataflow-meeting-insight

**Automated workflow to transcribe meetings, extract bullet points, and analyze SQL queries to solve business problems using AI.**

Este projeto utiliza inteligência artificial (LangChain + LangGraph + GPT-4 + Whisper) para transformar reuniões gravadas em insights acionáveis e diagnósticos técnicos de queries SQL complexas.

---

## 🚀 Visão Geral

O `dataflow-meeting-insight` é um pipeline inteligente de dados que automatiza o seguinte processo:

1. 🎙️ **Transcreve** vídeos de reuniões com a API do Whisper.
2. 🧠 **Extrai bullets técnicos** e decisões de negócio com GPT-4.
3. 🧾 **Analisa queries SQL** complexas (com OUTER APPLY, subqueries, etc.).
4. 📝 **Gera um relatório final** com diagnóstico e recomendações.

---

## ⚙️ Stack Tecnológica

- **[LangChain](https://www.langchain.com/)** – Framework de agentes LLM
- **[LangGraph](https://www.langchain.com/langgraph)** – Fluxo de estados baseado em agentes
- **[OpenAI Whisper API](https://platform.openai.com/docs/guides/speech-to-text)** – Transcrição de áudio/vídeo
- **[OpenAI GPT-4 Turbo](https://platform.openai.com/docs/guides/gpt)** – Processamento de linguagem natural
- **Python 3.10+**

---

## 🧱 Estrutura de Diretórios

```bash
lang-pipeline/
├── agents/                 # Agentes para cada etapa
│   ├── transcription_agent.py
│   ├── summary_agent.py
│   ├── sql_analysis_agent.py
│   └── output_agent.py
├── graph/                  # Fluxo LangGraph
│   └── pipeline_graph.py
├── data/
│   ├── input/              # Arquivos de entrada (vídeos, queries)
│   └── output/             # Relatórios gerados
├── main.py                 # Script principal de execução
├── .env                    # Chave da API OpenAI
├── requirements.txt
└── README.md
