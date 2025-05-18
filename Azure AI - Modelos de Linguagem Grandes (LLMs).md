# 🤖 Modelos de Linguagem Grandes (LLMs) e Azure AI

Descrevendo os conceitos de LLMs (Large Language Models), arquitetura Transformer, serviços Azure OpenAI e melhores práticas de IA generativa.

---

## 📚 O que são LLMs?

**LLMs (Large Language Models)** são redes neurais treinadas em enormes volumes de texto para compreender, gerar e completar linguagem natural de forma coerente e contextualizada.

---

## 🔧 Arquitetura Transformer

O Transformer é o principal bloco de construção de LLMs modernos, composto por duas partes:

### 1. Codificador (Encoder)
- Gera representações semânticas dos tokens de entrada.
- Estrutura em camadas de _Feed Forward_ e _Atenção_.

### 2. Decodificador (Decoder)
- Usa as mesmas camadas para gerar novas sequências de linguagem.
- Recebe as representações do codificador e produz tokens de saída.

### Etapas do Pipeline Transformer
1. **Tokenização**  
   Converte texto bruto em tokens numéricos (palavras, subpalavras ou caracteres).  
2. **Inserções (Embeddings)**  
   Atribui a cada token um vetor de alta dimensão que captura seu significado.  
3. **Atenção (Self-Attention)**  
   Cada token “olha” para todos os outros, ponderando quais são mais relevantes para o contexto.  
4. **Decodificação**  
   Baseado nos pesos de atenção, o decodificador prevê o próximo token mais provável até formar uma sequência completa.  

![Arquitetura Transformer](https://github.com/user-attachments/assets/f5fc754a-5f1f-4b84-9329-79d72c97d4eb)


---

## ☁️ Azure OpenAI Service

Permite **implantação**, **personalização** e **hospedagem** de LLMs (GPT-4, GPT-3, DALL·E, Embeddings) com segurança corporativa e ferramentas de governança:

- **Detecção e mitigação de uso prejudicial**  
- **RBAC** (controle de acesso baseado em funções)  
- Interfaces: Azure AI Studio, REST API, SDKs  
- Suporte a **Incorporação de Texto** para buscas semânticas  

---

## ✍️ IA Generativa

IA generativa cria conteúdo original a partir de prompts em linguagem natural:

- Texto: artigos, resumos, diálogos  
- Imagens: ilustrações via DALL·E  
- Código: snippets, scripts  
- Dados: tabelas, JSON  

---

## 🛡️ Responsabilidade no Uso de IA Generativa

1. **Identificar**  
   Riscos e possíveis danos (viés, desinformação, conteúdo impróprio).  
2. **Medir**  
   Avaliar impacto dos danos nas saídas geradas.  
3. **Mitigar**  
   Implementar controles (filtragem, moderação, validação humana).  
4. **Operar**  
   Documentar políticas, configurar permissões, realizar testes de segurança e integridade.

---

## 🧑‍💻 Copilots

Copilots são agentes de IA generativa integrados a aplicações (IDE, CRM, Office):

- Fornecem sugestões de código, respostas a e‑mails, insights em planilhas.  
- Aprendem com o contexto do usuário e personalizam recomendações.  

---
