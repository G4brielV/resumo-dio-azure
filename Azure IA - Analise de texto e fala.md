# Azure Speech Studio & Language Studio

Integração com Azure para serviços de IA focados em reconhecimento de fala, análise de texto e geração de áudio.

---

## 🚀 Visão Geral

- **Speech Studio**  
  Ferramenta para:
  - **Transcrição de áudio** → converte fala em texto com alta precisão.
  - **Síntese de voz** → gera áudio a partir de texto (text-to-speech) com vozes naturais.

- **Language Studio**  
  Conjunto de APIs para:
  - **Análise semântica** de texto ou fala.
  - **Extração de frases‑chave** → destaca palavras e trechos que carregam o sentido principal.
  - **Análise de sentimento** → classifica emoções (positivo, negativo, neutro) com base em adjetivos e tom.
  - **Reconhecimento de idioma** → detecta automaticamente o idioma do texto ou transcrição.
  - **Detecção de entidades** → identifica nomes de pessoas, locais, datas, produtos, etc.
  - **Detecção de intenção** → compreende o propósito do usuário (ex.: reservar voo, consultar saldo).

---

## 🔧 Funcionalidades Principais

| Recurso                   | Speech Studio             | Language Studio                         |
|---------------------------|---------------------------|-----------------------------------------|
| Transcrição de fala       | ✔️                        | (via API de texto após transcrição)     |
| Síntese de voz            | ✔️                        | —                                       |
| Detecção de idioma        | (configurável no serviço) | ✔️ automático                           |
| Análise de frases‑chave   | —                         | ✔️                                      |
| Análise de sentimento     | —                         | ✔️                                      |
| Extração de entidades     | —                         | ✔️                                      |
| Detecção de intenção      | —                         | ✔️                                      |

---

## 🧠 Como Funciona a Análise de Linguagem

1. **Detecção de Idioma**  
   - Identificado automaticamente pelo **Language Studio** ao enviar um trecho de texto ou transcrição.  
   - Suporta dezenas de idiomas sem necessidade de configuração prévia.

2. **Extração de Frases‑Chave**  
   - O serviço escaneia o texto em busca de termos com maior relevância semântica.  
   - Útil para resumo automático, indexação e geração de highlights em chats e relatórios.

3. **Análise de Sentimento**  
   - Classifica texto em **Positivo**, **Negativo** ou **Neutro**.  
   - Baseada em vocabulário e entonação: adjetivos, advérbios e construções que expressem emoção.

4. **Reconhecimento de Entidades**  
   - Identifica e classifica entidades como **Pessoas**, **Organizações**, **Locais**, **Datas**, **Produtos**, etc.  
   - Permite enriquecer bancos de dados, realizar buscas semânticas e alimentar chatbots.

5. **Detecção de Intenção**  
   - Mapeia frases de usuário para intenções predefinidas (ex.: “marcar reunião”, “consultar saldo”, “fazer reclamação”).  
   - Essencial para bots conversacionais e sistemas de atendimento automático.

---

## 💡 Principais Casos de Uso

- **Chatbots e Assistentes Virtuais**  
  - **Input**: fala do usuário transcrita e enviada ao Language Studio.  
  - **Processamento**: detecção de intenção + entidades + sentimento + frases‑chave.  
  - **Output**: resposta baseada em regras ou IA, síntese de voz opcional via Speech Studio.

- **Análise de Feedback**  
  - Transcreve gravações de suporte ou entrevistas.  
  - Extrai sentimento e tópicos recorrentes para relatórios de NPS e melhoria de produtos.

- **Legendagem e Closed Captions**  
  - Geração automática de legendas precisas para vídeos e transmissões ao vivo.

- **Aprendizado de Idiomas**  
  - Detecta e transcreve pronúncias de aprendizes, analisa erros e fornece dicas de correção.
