# 🚀 IA Ativa: RAG e Grafos no Varejo com NotebookLM

## 🎯 Contexto e Objetivos
Este projeto explora a implementação de **Sistemas RAG (Retrieval-Augmented Generation)** e **GraphRAG** como ferramentas estratégicas para o setor de varejo. O objetivo é utilizar o **NotebookLM** para sintetizar conhecimentos de fontes de alta relevância técnica (AWS, LuizaLabs, NVIDIA) e criar um guia que conecte a teoria de recuperação de informações com a prática de engenharia de software.

---

## 📚 Curadoria de Fontes
*Selecionei fontes que conectam a infraestrutura global da AWS com a visão prática e inovadora do LuizaLabs, permitindo uma visão 360° sobre IA no e-commerce.*

| Categoria | Fonte / Documento | Descrição e Relevância |
| :--- | :--- | :--- |
| **Infra & Cloud** | [Building Blocks (AWS)](https://aws.amazon.com/pt/blogs/industries/building-blocks-for-modern-retail-ecommerce-and-media-search-with-aws/) | Pilares de arquitetura para sistemas de busca modernos e escaláveis. |
| **Implementação** | [LangChain Python](https://docs.langchain.com/oss/python/langchain/overview) | Documentação base para orquestração de correntes e agentes inteligentes. |
| **Inovação** | [GraphRAG (LuizaLabs)](https://medium.com/luizalabs/construindo-rags-com-grafos-4bc6076f01a8) | Artigo técnico sobre o uso de grafos para melhorar o contexto da recuperação. |
| **Visão de Negócio** | [IA no Magalu (RI)](https://ri.magazineluiza.com.br/Download.aspx?Arquivo=F+gcCuq0PbMeHFIzyzqDKA==) | Relatório oficial sobre o impacto da IA Generativa na jornada do cliente. |
| **Métricas** | [RAGAS Framework](https://docs.ragas.io/en/stable/) | Ferramenta essencial para medir precisão e reduzir alucinações da IA. |
| **Impacto Varejo** | [AI in Retail (NVIDIA)](https://www.nvidia.com/en-us/industries/retail/) | Insights sobre busca semântica e conversão de vendas. |
| **Segurança** | [OWASP for LLM](https://owasp.org/www-project-top-10-for-large-language-model-applications/) | Diretrizes críticas para proteção contra injeções de prompt e vulnerabilidades. |

---

## 🛠️ Engenharia de Prompts e "Cicatrizes"

Abaixo, documento a evolução da interação com o NotebookLM e as dificuldades encontradas para extrair respostas tecnicamente precisas.

#### 1. O "Prompt de Aquecimento" (Iniciante)
> **Prompt:** "Com base em todas as fontes fornecidas, faça um resumo de 5 linhas destacando os pilares de RAG, Grafos, Segurança e Varejo."

<details>
<summary><b>Clique para expandir o Resultado</b></summary>
O modelo RAG aprimora LLMs combinando conhecimento pré-treinado com bases externas, reduzindo alucinações. A evolução para GraphRAG melhora o raciocínio lógico em consultas complexas ao mapear relações entre documentos. A indústria adota padrões de engenharia como evals, guardrails e cache para robustez. No e-commerce, a IA revoluciona buscas com machine learning e ranqueamento personalizado. Operações omnicanal são otimizadas via IA e simulação para prevenir perdas e gerir estoques.
</details>

**Resultado:** ⭐⭐⭐⭐ | **Observações:** O desafio foi manter a densidade técnica em 5 linhas. A "cicatriz" aqui foi a tendência da IA em ser genérica, exigindo iteração para incluir a camada de segurança da OWASP.

#### 2. O "Prompt Estruturante" (Intermediário)
> **Prompt:** "Como o GraphRAG (Jackson/LuizaLabs) melhora os 'Building Blocks' da AWS? Responda em 5 linhas."

<details>
<summary><b>Clique para expandir o Resultado</b></summary>
Os 'Building Blocks' da AWS utilizam correspondência lexical e similaridade vetorial (kNN) para recuperar documentos isoladamente. O GraphRAG aprimora esse processo ao mapear relações explícitas entre conceitos por meio de nós e arestas. Enquanto a busca da AWS pode sofrer com falta de contexto estrutural, os grafos identificam conexões implícitas e resolvem redundâncias. Consequentemente, o GraphRAG fortalece o módulo de correspondência da AWS com raciocínio lógico e inferência.
</details>

**Resultado:** ⭐⭐⭐⭐⭐ | **Observações:** A IA inicialmente tratou Grafos e Vetores como tecnologias rivais. O refinamento foi necessário para apresentá-los como camadas complementares de arquitetura.

#### 3. O "Prompt de Especialista" (Avançado)
> **Prompt:** "Atue como Engenheiro Sênior do LuizaLabs. Desenvolva um plano RAG com FastAPI e LangChain seguindo OWASP e RAGAS. Liste riscos de alucinação. Responda em 5 linhas."

<details>
<summary><b>Clique para expandir o Resultado</b></summary>
As fontes não detalham FastAPI, LangChain ou RAGAS. O plano viável utiliza Python com NetworkX para grafos e Ollama para embeddings. A arquitetura funciona expandindo a busca vetorial para nós vizinhos no grafo. Para segurança, deve-se incorporar guardrails e evals automatizados (como G-Eval) no lugar de métricas convencionais. O risco de alucinação ocorre quando a busca falha no escopo de negócio, como sugerir "papel de impressão" em uma loja exclusiva de sapatos.
</details>

**Resultado:** ⭐⭐⭐⭐⭐ | **Observações:** Este teste revelou a **honestidade intelectual** da IA. Ela se recusou a inventar dados sobre FastAPI (não presentes nas fontes) e propôs uma alternativa técnica baseada na lógica de Grafos extraída dos documentos.

---

## 🚀 Próximos Passos: Da Teoria à Prática

Como Engenheiro de Computação, utilizei o **NotebookLM** para consolidar a base teórica. Abaixo, apresento a validação prática que realizei para transpor esse conhecimento para o código.

### 🛠️ Validação Experimental: Agente LangChain + SQLite

🔗 **Repositório do experimento:** [Acessar no GitHub](https://github.com/FabioRSJunior/Estudo_llms/tree/main/Projeto%2003%20-%20introdu%C3%A7%C3%A3o%20a%20Agentes)


Desenvolvi um **Agente Offline** para validar a capacidade de interpretação semântica em bancos de dados estruturados (SQL), complementando o estudo de RAG.

* **O Desafio:** Validar o "Text-to-SQL" automático sem funções de busca manuais.
* **Pergunta:** *"Quais interesses em comum de Fabio e Zyphor?"*
* **Ação:** O agente interpretou a pergunta -> Gerou Query SQL -> Consultou o banco.
* **Resposta:** *"The common interests between Fabio and Zyphor are Inteligência Artificial, Machine Learning, Deep Reinforcement Learning..."*

**Conclusão:** O **RAG** (estudado via NotebookLM) e o **Agente SQL** (validado em código) formam a arquitetura completa para o varejo: um consulta o conhecimento (PDFs), o outro a realidade transacional (Estoque/Preços).

---

## 📖 Miniguia de Estudo (Entrega Final)

### Glossário "Straight to the Point"
* **RAG:** Técnica de "dar um livro" para a IA ler antes de responder, reduzindo erros.
* **GraphRAG:** Evolução que usa grafos (nós e arestas) para a IA entender o contexto entre produtos.
* **Alucinação:** Quando a IA inventa uma informação por falta de dados na fonte.
* **Text-to-SQL:** Capacidade da IA de converter linguagem natural em consultas de banco de dados precisas.
