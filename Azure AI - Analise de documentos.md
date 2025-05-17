# Azure AI Document Intelligence

O **Azure AI Document Intelligence** é um serviço de inteligência artificial voltado para a análise e compreensão automática de documentos. Ele extrai informações relevantes a partir de documentos digitalizados, PDFs ou imagens, convertendo conteúdo não estruturado em dados estruturados e utilizáveis.

---

## 🧠 O que é?

O **Document Intelligence** (anteriormente conhecido como Form Recognizer) usa modelos de IA para identificar regiões de interesse em documentos e extrair valores-chave, como nomes, datas, totais, números de fatura, entre outros.  
Essa inteligência pode ser usada em documentos genéricos ou com layouts específicos, permitindo desde o reconhecimento padrão até treinamentos personalizados.

---

## ⚙️ Como Funciona?

O processo ocorre em três etapas principais:

1. **Pré-processamento:** o documento (PDF, imagem, escaneamento, etc.) é analisado visualmente e textualmente.
2. **Extração de dados:** regiões de interesse são identificadas com base em texto, layout e estrutura. Dados são extraídos conforme modelos pré-definidos ou personalizados.
3. **Retorno estruturado:** os dados são retornados como JSON com pares chave-valor, tabelas ou campos personalizados.

---

## 🧩 Recursos Principais

- **Extração de Pares Chave–Valor:** identifica campos como “Nome”, “Endereço”, “Total”, etc.
- **Reconhecimento de Tabelas:** detecta tabelas e retorna dados tabulares organizados.
- **Leitura Óptica (OCR) Inteligente:** lê documentos escaneados e imagens com alta precisão.
- **Modelos Pré-treinados:** disponíveis para faturas, recibos, contratos, identidades, etc.
- **Modelos Customizados:** você pode treinar o serviço para entender qualquer layout específico de documento.
- **Detecção de Relacionamentos:** conecta informações correlacionadas, como valores monetários e seus respectivos campos.

---

## 📄 Tipos de Documentos Suportados

- PDFs (nativos ou escaneados)
- Imagens (JPG, PNG, TIFF, BMP)

---

## 🧠 Modelos Disponíveis

| Tipo de Modelo | Descrição |
|----------------|-----------|
| **Pré-construído** | Já treinados para entender documentos comuns como faturas, IDs e contratos |
| **Customizado** | Treinados por você com seus próprios documentos (sem necessidade de anotação manual no v3.0) |
| **Layout** | Foco apenas em layout: extrai texto, estrutura e localização visual |
| **Read OCR** | Somente leitura de texto (OCR puro) |

