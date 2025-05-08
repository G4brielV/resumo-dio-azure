# ☁️ Computação em Nuvem - Anotações do Bootcamp Java Cloud Native (Bradesco / DIO)

Este repositório contém anotações e resumos sobre os principais conceitos de computação em nuvem estudados no bootcamp **Java Cloud Native**, promovido pelo **Bradesco** em parceria com a **DIO**.

---

## 📘 O que é Computação em Nuvem?

Computação em nuvem é a entrega de serviços de computação (como servidores, armazenamento, redes, bancos de dados, software etc.) por meio da Internet.  
Diferente do modelo tradicional com infraestrutura local, na nuvem os recursos são fornecidos por terceiros, sob demanda.

---

## ☁️ Tipos de Nuvem

### 🔒 Nuvem Privada  
Ambiente de nuvem exclusivo de uma organização. A empresa é responsável por toda a estrutura: segurança, manutenção, atualizações de hardware etc.

### 🌐 Nuvem Pública  
Ambiente de nuvem em que os recursos são disponibilizados por provedores terceirizados via Internet. Qualquer pessoa ou empresa pode utilizá‑los sob demanda.

### 🔁 Nuvem Híbrida  
Modelo que combina recursos da nuvem pública com a nuvem privada ou infraestrutura local, permitindo maior flexibilidade e controle.

---

## 💰 CapEx vs OpEx na Nuvem

|                             | CapEx (Capital Expenditure)                  | OpEx (Operational Expenditure)               |
|-----------------------------|----------------------------------------------|----------------------------------------------|
| Tipo de nuvem associado     | Nuvem Privada                                | Nuvem Pública                                |
| Gasto inicial               | Alto (compra de infraestrutura)              | Nenhum                                       |
| Custo ao longo do tempo     | Diminui, apenas manutenção do ambiente       | Varia conforme o uso                         |

---

## 🌟 Benefícios da Computação em Nuvem

| Benefício           | Descrição                                                                                                                                                  |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Disponibilidade      | Recursos sempre disponíveis de acordo com o SLA (Service Level Agreement). Se o provedor não cumprir, são concedidos créditos aos clientes afetados.        |
| Escalabilidade       | Ajuste rápido de capacidade (memória, CPU, armazenamento) para atender a diferentes cenários de carga.                                                       |
| Elasticidade         | Adição e remoção automática de VMs conforme a demanda, evitando gargalos e reduzindo custos em períodos de baixo uso.                                        |
| Confiabilidade       | Arquitetura descentralizada: falhas em uma região não comprometem o serviço como um todo, pois outras regiões continuam operando.                             |
| Previsibilidade      | Desempenho e custos estáveis — você sabe antecipadamente o que esperar em termos de gasto e capacidade.                                                       |
| Segurança            | Ferramentas avançadas de segurança são oferecidas pelo provedor; cabe ao cliente configurar e gerenciar OS, softwares e regras de acesso.                   |
| Governança           | Monitoramento de conformidade: a nuvem sinaliza desvios em relação a políticas corporativas, regulatórias ou governamentais.                                   |
| Gerenciabilidade     | Múltiplas interfaces de gestão: APIs, linha de comando, consoles web e SDKs permitem automação e integração com processos existentes.                         |

---

## 📜 SLA (Service Level Agreement)

O SLA é um contrato que define níveis mínimos de disponibilidade, desempenho e suporte que o provedor deve cumprir.  
- **Métricas comuns**: disponibilidade (% uptime), tempo de resposta, tempo de reparo.  
- **Créditos e penalidades**: se o provedor não atingir o SLA, o cliente recebe créditos proporcionais na fatura (ex.: 10% de downtime gera 10% de crédito).  

---

## 🛠️ Tipos de Serviço em Nuvem

| Sigla     | Nome                            | Responsabilidade do Cliente                                                | Responsabilidade do Provedor                   | Custo Relativo | Quando usar                                                                                       |
|-----------|---------------------------------|----------------------------------------------------------------------------|------------------------------------------------|----------------|---------------------------------------------------------------------------------------------------|
| On‑Prem   | On‑Premises                     | Todas as camadas: dados, apps, OS, rede, hardware, datacenter               | –                                              | Alto           | Quando você precisa de controle total sobre infraestrutura física e políticas de segurança locais |
| IaaS      | Infrastructure as a Service     | Configuração e manutenção de VMs, rede, storage, backups e atualizações de OS | Fornece hardware virtualizado e rede            | Alto           | Controle sobre o sistema operacional e ambiente de execução, sem gerenciar hardware físico       |
| PaaS      | Platform as a Service           | Gerenciamento da aplicação e configurações de software                       | Gerencia infraestrutura e OS                    | Médio          | Focar no desenvolvimento e deployment de apps, sem se preocupar com infraestrutura subjacente    |
| SaaS      | Software as a Service           | Uso e configuração de aplicativos finais; gestão de usuários e permissões     | Gerencia tudo: infraestrutura, OS e software    | Baixo          | Aplicação pronta para uso, sem qualquer gestão de infraestrutura, SO ou instalação de software   |


---
