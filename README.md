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

## 🏗️ Componentes de Arquitetura do Azure

### 🌍 Região (Region)  
- **Definição**: Conjunto de data centers geograficamente próximos, geralmente 3 por região.  
- **Alta disponibilidade**: Data centers replicam e sincronizam dados entre si. Se um DC falhar, os demais continuam operando (mesmo que com desempenho reduzido).  
- **Responsabilidade do provedor**: O Azure “possui” o recurso físico; você “possui” os dados. O provedor garante conformidade com normas como a LGPD.

### 🔄 Pares de Região (Paired Regions)  
- **Objetivo**: Recuperação de desastres quando uma região inteira fica indisponível.  
- **Características**:  
  - Região secundária automática para fail‑over.  
  - Nem sempre oferece o conjunto completo de serviços da região primária, mas supre o essencial.

### 🛡️ Regiões Soberanas (Sovereign Regions)  
- **Uso**: Atendem requisitos legais ou governamentais específicos.  
- **Exemplos**:  
  - Azure Government (EUA, para uso militar e agências governamentais).  
  - Azure China (operado pela 21Vianet, conforme legislação chinesa).

---

### 🏢 Zona de Disponibilidade (Availability Zone)  
- **Definição**: Agrupamento de vários data centers isolados dentro de uma mesma região.  
- **Objetivo**:  
  - Isolamento físico de falhas — se um DC em uma zona cair, VMs em outra zona continuam ativas.  
  - Garantir continuidade de serviço e reduzir pontos únicos de falha.

### 🔧 Conjuntos de Disponibilidade (Availability Sets)  
- **Fault Domains (Domínios de Falha)**  
  - VMs distribuídas em racks físicos distintos.  
  - Protege contra falhas de hardware ou falta de energia em um único rack.  
- **Update Domains (Domínios de Atualização)**  
  - VMs agrupadas para atualizações sequenciais.  
  - Evita downtime simultâneo durante manutenção da plataforma Azure.

## 📌 Responsabilidades de Availability Set vs. Availability Zone

| Recurso            | Protege contra falha de…   | Nível de isolamento  | Escopo de cobertura         |
|--------------------|----------------------------|----------------------|-----------------------------|
| Availability Set   | Rack (Fault Domain)        | Dentro de uma zona   | VMs em racks distintos      |
| Availability Zone  | Zona inteira (data centers) | Entre zonas da região | Zonas geograficamente isoladas |

---


### 📦 Grupo de Recursos (Resource Group)  
- **Função**: Contêiner lógico para organizar recursos (VMs, Storage Accounts, redes, etc.).  
- **Regras**:  
  - Cada recurso pertence a um único grupo.  
  - Recursos podem ser movidos entre grupos.  
  - Grupos **não** podem ser renomeados.  
  - Recursos dentro de um grupo podem estar em regiões diferentes.

### 🔑 Assinaturas (Subscriptions)  
- **Modelo**: Uma conta Azure pode ter múltiplas assinaturas; cada assinatura está vinculada a uma única conta.  
- **Uso**:  
  - Separa faturamento e limites de serviço.  
  - Permite delegar acesso e controlar gastos por projeto ou equipe.

### 🗂️ Grupos de Gerenciamento (Management Groups)  
- **Objetivo**: Aplicar políticas, RBAC e compliance de forma hierárquica sobre múltiplas assinaturas.  
- **Hierarquia**: Para aplicar políticas e RBAC sobre múltiplas subscriptions.  

---

## ☁️ Termos e Componentes na Azure e Equivalentes em Outros Provedores

| Conceito Azure              | AWS                                         | GCP                                          |
|-----------------------------|---------------------------------------------|----------------------------------------------|
| Região (Region)             | Region                                      | Region                                       |
| Zona de Disponibilidade     | Availability Zone (AZ)                      | Zone                                         |
| Resource Group              | Tags / Projects¹                            | Project / Folder                             |
| Subscription                | Account / AWS Organizations                 | Project                                      |
| Management Group            | AWS Organizations / Organizational Units     | Organization / Folder                       |
| Paired Regions              | Region Pair                                 | — (via multi‑region replication)             |
| Sovereign Regions           | AWS GovCloud / China Regions                | — (Cloud China via parceiros)                |
| Availability Set            | Placement Group                             | — (políticas de instâncias semelhantes)      |


## 🖥️ Máquinas Virtuais (VMs)

### 💻 VMs (IaaS)  
Emulação completa de um computador físico na nuvem, incluindo CPU, memória, armazenamento e interfaces de rede.  
- **Uso**: lift‑and‑shift de aplicações legadas, teste de SOs, ambientes isolados.  
- **Vantagem**: controle total do sistema operacional e software instalado.  

### 🧩 Conjuntos de Dimensionamento de VMs (VM Scale Sets)  
Gerenciam grupos de VMs idênticas com escalonamento automático baseado em métricas de uso.  
- **Balanceamento de carga** automático entre instâncias.  
- **Escalabilidade horizontal**: adiciona/remove VMs conforme demanda.  

### 🏗️ Conjuntos de Disponibilidade de VMs (Availability Sets)  
Agrupam VMs semelhantes e as distribuem em racks físicos isolados dentro de um data center para maximizar disponibilidade.  
- **Domínios de Falha (Fault Domains)**  
  - Racks físicos distintos.  
  - Evitam indisponibilidade por falhas de hardware ou energia em um rack específico.

- **Domínios de Atualização (Update Domains)**  
  - Grupos de VMs que podem ser reiniciadas simultaneamente durante atualizações do Azure.  
  - Garante que atualizações de manutenção não impactem todas as instâncias ao mesmo tempo.
    
> ![Availability Set Illustration](https://github.com/user-attachments/assets/b6893718-f8e0-4dd0-b781-b3f2082df1a6)


---

## 🧑‍💻 Área de Trabalho Virtual (DaaS)

### 🌐 Azure Virtual Desktop (DaaS)  
Desktop completo (SO, apps, dados) entregue pela nuvem e acessado remotamente.  
- **Benefícios**:  
  - Gerenciamento centralizado e segurança (MFA, políticas de acesso).  
  - Redução de risco de dados em endpoints.  
  - Provisionamento dinâmico de desktops.  
- **Modelos**:  
  - **Multissessão**: vários usuários em uma mesma VM Windows.  
  - **VMs dedicadas**: cada usuário com sua própria VM.  

### 🔍 Diferença: VMs vs. Área de Trabalho Virtual  

- 📦 **Máquina Virtual (VM)**: é como alugar um galpão vazio. Você escolhe o que vai colocar lá: máquinas, móveis, servidores, etc. É flexível, mas você precisa configurar tudo.
- 🖥️ **Área de Trabalho Virtual**: é como alugar um escritório já mobiliado. Você entra, liga o computador e já começa a trabalhar — tudo pronto, acessível de qualquer lugar.

#### Resumo:
| Característica       | VM (Máquina Virtual)          | Área de Trabalho Virtual               |
|----------------------|-------------------------------|----------------------------------------|
| **Foco**             | Infraestrutura e servidores   | Experiência do usuário (desktop remoto) |
| **Configuração**     | Você instala e configura tudo | Já vem com ambiente de trabalho pronto |
| **Público-alvo**     | Admins, desenvolvedores       | Funcionários, equipes remotas          |
| **Acesso**           | Mais técnico e indireto       | Interface gráfica pronta para uso      |

---

## 🐳 Contêineres no Azure 
Ambiente leve que executa aplicações empacotadas sem gerenciar o SO completo. Responde rapidamente a demandas variáveis.

### ⚙️ Instâncias de Contêiner (Container Instances – PaaS)  
Executa um contêiner ou pod sob demanda, sem necessidade de orquestração.

### 🔄 Aplicativos de Contêiner (Container Apps – PaaS)  
- **Balanceamento de carga** automático entre instâncias de contêiner.  
- **Escalabilidade** horizontal automática conforme métricas (CPU, fila, HTTP).  

### 🧠 AKS – Azure Kubernetes Service  
Plataforma gerenciada de Kubernetes para orquestrar contêineres em produção.  
- Automatiza deploy, escalonamento, monitoramento e atualizações de clusters.  

---

## ⚡ Azure Functions

### 🔧 Azure Functions (PaaS)  
Execução de código “serverless” acionado por eventos (HTTP, mensagens, timers).  
- **Cobra** por execução e tempo de execução.  
- Ideal para pequenas tarefas, pipelines de dados e automações event‑driven.  

---

## 🌐 Serviços de Aplicativos

### 🌍 App Service (PaaS)  
Hospedagem gerenciada de aplicações Web, APIs e mobile back‑ends.  
- **Recursos**:  
  - Deploy contínuo (Git, CI/CD).  
  - Slots de staging.  
  - SSL/TLS integrado.  
  - Autenticação/Autorização built‑in.  

---

## 🌐 Redes no Azure

### 🔌 Rede Virtual (VNet)  
Rede isolada onde recursos Azure se comunicam.  
- VNets não se conectam por padrão; use peering, VPN ou ExpressRoute.

### 🔐 Gateway de VPN  
Cria túneis IPsec/IKE entre VNet e rede on‑premises pela Internet pública.

### 🚄 ExpressRoute  
Conexão privada (cabo dedicado) entre datacenter local e Azure, sem passar pela Internet pública.

### 🌍 DNS do Azure  
Serviço DNS gerenciado para:  
- Domínios públicos e privados.  
- Resolução de nomes dentro de VNets.  
- Zonas DNS customizadas e políticas de tráfego.


## 🔐 Serviços de Diretório

### 🆔 Microsoft Entra ID  
Serviço de gerenciamento de identidade e acesso na nuvem, criado e mantido por você.  
- **Autenticação**: valida credenciais dos usuários.  
- **SSO (Single Sign-On)**: login único salva credenciais para múltiplos apps.  
- **Gerenciamento de aplicativos e dispositivos**: controle centralizado de acesso.  
- **B2B (Business-to-Business)**: convida identidades externas para acessar recursos da sua organização.  
- **B2C (Business-to-Consumer)**: permite que usuários externos (Google, Facebook etc.) usem suas credenciais para acessar seu app.  
- **Domínio Gerenciado**: sincroniza contas on-premises para Entra ID, mantendo réplicas dos usuários na nuvem.

---

## 🔑 Métodos de Autenticação & Autorização

- **Autenticação**: processo de verificar “quem você é” (usuário/senha, certificado, token).  
- **Autorização**: define “o que você pode fazer” dentro do sistema após autenticado.  
- **MFA (Autenticação Multifator)**: combina “algo que você sabe” (senha) + “algo que você tem” (celular, token) para maior segurança.

---

## 🛡️ Modelos de Segurança

- **Acesso Condicional**  
  Usa atributos de usuário, dispositivo, localização, aplicativo e risco para permitir ou bloquear acessos em tempo real.

- **RBAC (Role-Based Access Control)**  
  Concede permissões mínimas necessárias com base nas funções atribuídas aos usuários.

- **Zero Trust**  
  Princípio “nunca confiar, sempre verificar”: todas as solicitações são autenticadas, autorizadas e criptografadas.

- **Defesa em Profundidade**  
  Abordagem em camadas de proteção:  
  1. **Físico**: controle de acesso a datacenters, vigilância, biometria.  
  2. **Identidade & Acesso**: gestão de identidades, SSO, MFA, políticas de senha.  
  3. **Perímetro**: firewalls de borda, DDoS Protection, Web Application Firewall (WAF).  
  4. **Rede**: Network Security Groups (NSGs), Azure Firewall, segmentação de sub-redes.  
  5. **Computação**: hardening de sistemas operacionais, patches automáticos, antimalware.  
  6. **Aplicativo**: Application Gateway, App Service Environment, análise de código e WAF de aplicação.  
  7. **Dados**: criptografia em repouso e em trânsito, Azure Key Vault, classificação e DLP.

- **Microsoft Defender para Nuvem**  
  Monitoramento contínuo e proteção contra ameaças em VMs, containers e serviços na nuvem.  


