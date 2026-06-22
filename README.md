# ☁️ Guia de Estudos e Anotações: Microsoft Azure

Este repositório contém um resumo estratégico, anotações de aula e dicas práticas sobre os fundamentos da computação em nuvem com foco na plataforma **Microsoft Azure**. Ideal para consultas rápidas no dia a dia e preparação para certificações (como a AZ-900).

---

## 📌 Sumário
* [1. Conceitos Fundamentais de Nuvem](#1-conceitos-fundamentais-de-nuvem)
* [2. Modelos de Serviço (IaaS, PaaS, SaaS)](#2-modelos-de-serviço-iaas-paas-saas)
* [3. Modelos de Nuvem (Pública, Privada, Híbrida)](#3-modelos-de-nuvem-pública-privada-híbrida)
* [4. Benefícios Principais da Azure](#4-benefícios-principais-da-azure)
* [5. Dicas Práticas e Governança](#5-dicas-práticas-e-governança)

---

## 1. Conceitos Fundamentais de Nuvem

### 💰 Aspectos Financeiros: CapEx vs. OpEx
A migração para a nuvem transforma a estratégia financeira das empresas, substituindo custos fixos por custos operacionais variáveis:

*   **CapEx (Capital Expenditure):** Investimento inicial em infraestrutura física (compra de servidores, racks, cabeamento, construção de Data Centers). Exige alto capital inicial e desvaloriza com o tempo.
*   **OpEx (Operational Expenditure):** Despesas operacionais diárias/mensais. Na nuvem, você paga apenas pelo que consome (*Pay-as-you-go*), eliminando custos de manutenção física e ociosidade de hardware.

### 📊 Modelo Baseado em Consumo
*   Não há custos iniciais com infraestrutura bruta.
*   Pagamento retroativo baseado no uso exato de processamento, memória e armazenamento.
*   Permite uma **melhor previsão de custos** por meio de ferramentas de análise histórica de dados de tráfego.

---

## 2. Modelos de Serviço (IaaS, PaaS, SaaS)

O nível de gerenciamento e controle do ambiente varia de acordo com o modelo de serviço escolhido.

```text
 ──► Maior gerenciamento pelo Usuário / Menos abstração
┌────────────────────────────────────────────────────────┐
│ On-Premises ──► Infraestrutura física local (100% você)│
├────────────────────────────────────────────────────────┤
│ IaaS ─────────► Servidores brutos e redes virtuais     │
├────────────────────────────────────────────────────────┤
│ PaaS ─────────► Ambientes prontos para hospedar código │
├────────────────────────────────────────────────────────┤
│ SaaS ─────────► Software pronto por assinatura (Web)   │
└────────────────────────────────────────────────────────┘
 ──► Menor gerenciamento pelo Usuário / Maior abstração
```

### 🧱 IaaS (Infraestrutura como Serviço)
*   **O que é:** O provedor entrega o hardware virtualizado básico.
*   **Seu gerenciamento:** **Máximo**. Você é responsável por instalar, atualizar e manter o Sistema Operacional (Windows/Linux), além de gerenciar firewalls, middlewares e bancos de dados.
*   **Exemplo na Azure:** *Azure Virtual Machines (VMs)*.

### ⚙️ PaaS (Plataforma como Serviço)
*   **O que é:** O provedor gerencia o hardware e o Sistema Operacional. 
*   **Seu gerenciamento:** **Médio**. Você foca exclusivamente no desenvolvimento, implantação e configuração do seu código/aplicativo.
*   **Exemplo na Azure:** *Azure App Services, Azure SQL Database*.

### 🌐 SaaS (Software como Serviço)
*   **O que é:** Aplicativo totalmente pronto, hospedado e gerenciado pelo provedor.
*   **Seu gerenciamento:** **Mínimo**. Os usuários pagam pelo software em um modelo de assinatura e gerenciam apenas os dados inseridos, dispositivos e permissões de acesso.
*   **Exemplo na Azure/Microsoft:** *Microsoft 365, Microsoft Dynamics 365*.

---

## 3. Modelos de Nuvem (Pública, Privada, Híbrida)

*   **Nuvem Pública:** Recursos compartilhados (multilocação) de forma segura com várias empresas e usuários gerais. Acesso via internet pública.
*   **Nuvem Privada:** Infraestrutura dedicada exclusivamente a uma única organização (Data Center local ou *On-premises*). Controle total, mas sem a elasticidade automática da nuvem pública.
*   **Nuvem Híbrida:** **O modelo de maior flexibilidade**. Combina nuvens públicas e privadas ao mesmo tempo. Permite manter dados ultrassensíveis localmente por regulação e usar a nuvem pública para escalar processamento de forma ágil.
*   *Nota sobre Multinuvem (Multi-cloud):* É a estratégia de utilizar dois ou mais provedores de nuvem pública simultaneamente (ex: Azure + AWS).

---

## 4. Benefícios Principais da Azure

*   ⚡ **Elasticidade:** Capacidade de alocar ou desalocar recursos computacionais (escalabilidade dinâmica) de forma automática em tempo real para atender requisições externas com agilidade e rapidez.
*   🔄 **Alta Disponibilidade:** Garantia de que seus sistemas continuarão online e operando através de redundâncias geográficas, mitigando falhas de hardware ou energia.
*   🛠️ **Gerenciabilidade:** Facilidade de monitorar e gerenciar recursos remotamente utilizando o **Portal Azure (Web)**, **Azure CLI (Linha de Comando)** ou scripts de Infraestrutura como Código (IaC).
*   📜 **SLA (Service Level Agreement):** Contrato formal que garante os tempos mínimos de atividade (*uptime*) de cada serviço na nuvem, assegurando créditos financeiros se as metas de disponibilidade não forem cumpridas.

---

## 5. Dicas Práticas e Governança

### 🤝 Modelo de Responsabilidade Compartilhada
*   **Na nuvem (Provedor):** A Azure cuida da segurança física do hardware, da rede global e dos hipervisores.
*   **Da nuvem (Você):** Você sempre será responsável pela segurança dos seus **dados**, pela configuração de **permissões de acesso (IAM)** e pelas credenciais das contas.

### 💡 Dicas de FinOps e Economia na Azure
1.  **Azure Advisor:** Monitore as recomendações do Advisor semanalmente para identificar recursos ociosos e economizar dinheiro.
2.  **Orçamentos e Alertas:** Crie alertas de consumo no *Azure Cost Management* para ser notificado por e-mail antes de estourar o orçamento mensal estimado.
3.  **Tags (Etiquetas):** Utilize Tags em todos os recursos para organizar os custos por departamento (ex: `Ambiente: Producao`, `CentroDeCusto: TI`).

---
✍️ *Anotações organizadas para fixação de conceitos e melhores práticas em Cloud Computing.*
