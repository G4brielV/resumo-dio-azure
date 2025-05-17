# Azure Cognitive Search

O **Azure Cognitive Search** é um serviço de pesquisa na nuvem que combina indexação de documentos com capacidades de IA para criar experiências de busca avançadas.

---

## 🚀 Visão Geral

1. **Ingestão de Dados**  
   - Fontes suportadas:  
     - Blob Storage Containers  
     - Data Lake Storage  
     - Table Storage  
     - SQL, Cosmos DB (conectores adicionais)  

2. **Enriquecimento (AI Enrichment)**  
   - Usa operadores de Cognitive Services para:  
     - Processamento de Linguagem Natural (PLN)  
     - Visão Computacional (extração de texto de imagens)  
     - Tradução automática  
     - Análise de sentimento  
     - Extração de entidades e frases‑chave  
   - Converte conteúdo bruto em campos estruturados no índice de busca.

3. **Indexação**  
   - Criação de índice invertido com campos definidos (texto, número, data, localização, etc.).  
   - Suporte a filtros, facetas, sugestões e ordenação.

4. **Consulta e Exploração**  
   - APIs de busca com retorno em JSON.  
   - Sugestões de pesquisa (“type‑ahead”), autocompletar e “did‑you‑mean”.  
   - Facetamento para navegação por categorias.  
   - Visualizações customizadas

5. **Mineração de Conhecimento**  
   - Insights em escala: identificação de tendências, termos mais buscados e agrupamentos de tópicos.  
   - Painéis de controle e relatórios de uso.

---

## 🔧 Exemplo de Arquitetura

```mermaid
flowchart LR
  Storage["Storage Account (Blob, Table, Data Lake)"]
  AIService["Azure AI Services (PLN, Visão, Tradução)"]
  Indexer["Indexer (Cognitive Search)"]
  SearchAPI["Search API (Cognitive Search)"]
  Client["Aplicação Cliente (Web, App, Bot)"]

  Storage --> Indexer
  AIService --> Indexer
  Indexer --> SearchAPI
  Client --> SearchAPI
