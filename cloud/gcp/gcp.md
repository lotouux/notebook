
<div align="center">

# ☁️ Google Cloud Platform (GCP)

### A Nuvem do Google: Infraestrutura Global, Armazenamento, IaaS e a Revolução Serverless

</div>

---

<br>

<table align="center" width="850" cellpadding="18" style="border-collapse: collapse; background-color:#f8f1f5; border-radius:14px;">

<tr>

<td>

## 💡 1. A Fundação: GCP e Google Workspace (G Suite)

O Google Cloud Platform (GCP) não é apenas um serviço de hospedagem. É a oportunidade de operar sobre a mesma infraestrutura global construída para suportar gigantes como o Google Search e o YouTube.

---

### ☁️ GCP (Foco na Construção)

Ambiente voltado para desenvolvedores e arquitetos criarem aplicações, bancos de dados e servidores virtuais.

#### Características:
- Infraestrutura como Serviço (IaaS)
- Plataforma como Serviço (PaaS)
- Computação Serverless
- Pagamento por uso de recursos

---

### 🧩 Google Workspace (Foco em Produtividade)

Modelo SaaS voltado ao usuário final.

#### Serviços:
- Gmail Corporativo
- Google Meet
- Google Drive
- Google Docs e Planilhas

#### Modelo Financeiro:
- Cobrança mensal por usuário

---

## 📦 2. Opções de Armazenamento e Cloud Storage

O Google divide armazenamento em soluções de objetos e armazenamento em blocos.

---

### 💽 Persistent Disk

Discos duráveis utilizados diretamente nas Máquinas Virtuais.

#### Recursos:
- Snapshots
- Alta disponibilidade
- Integração nativa com VMs

---

### 🪣 Google Cloud Storage (Object Storage)

O principal serviço de armazenamento da plataforma.

Funciona através de repositórios globais chamados **Buckets**.

#### Características:
- Até 5 TB por arquivo
- Durabilidade de 99,999999999%
- Alta escalabilidade
- Segurança corporativa

---

### 💡 Pro Tip

Os nomes dos buckets precisam ser globalmente únicos.

Ou seja:
- ninguém no mundo pode ter o mesmo nome do seu bucket.

---

## 📊 Matriz de Decisão: Classes de Armazenamento

| Classe | Caso de Uso | Retenção Mínima | Custos |
|---|---|---|---|
| Standard | Dados acessados diariamente | Nenhuma | Armazenamento caro, acesso barato |
| Nearline | Backups mensais | 30 dias | Armazenamento moderado |
| Coldline | Disaster Recovery | 90 dias | Armazenamento barato |
| Archive | Arquivo morto e compliance | 365 dias | Armazenamento extremamente barato |

---

### 🚀 Diferencial do Google

No Archive Storage do Google, os dados continuam disponíveis em milissegundos, diferente de concorrentes que podem levar horas para restaurar arquivos frios.

---

## 🖥️ 3. Processamento: Compute Engine (IaaS)

O Compute Engine é o serviço de Infraestrutura como Serviço (IaaS) do GCP.

Ele permite criar:
- Máquinas Virtuais
- Containers
- Infraestrutura customizada

---

### 🎯 Diferenciais da Criação Visual

#### 📦 Catálogo de Sistemas Operacionais

- Debian
- Ubuntu
- Red Hat
- CentOS
- SUSE
- Windows Server
- Distribuições otimizadas pelo Google

---

### 💰 Calculadora em Tempo Real

Durante a criação da VM:
- CPU
- memória
- disco
- rede

atualizam automaticamente o custo estimado mensal.

---

### 🔄 Flexibilidade

Você pode:
- criar do zero
- usar templates
- importar VMs externas

---

## 🔐 Acesso Direto: SSH Nativo pelo Navegador

O GCP permite acessar máquinas Linux e Windows diretamente pelo navegador.

### Benefícios:
- Sem instalar programas locais
- Sem configurar clientes SSH externos
- Sem gerenciar chaves manualmente

Resultado:
- acesso remoto rápido e frictionless.

---

## ⚡ 4. App Engine e Cloud Functions (A Revolução Serverless)

Quando o foco é apenas o código, o Google oferece abstração máxima da infraestrutura.

---

### 🚀 App Engine (PaaS)

Serviço totalmente gerenciado para hospedar aplicações.

### Como funciona:
1. Escolha a linguagem
2. Faça upload do código
3. O Google provisiona:
   - servidores
   - escalabilidade
   - balanceamento
   - atualizações

---

### 🌎 Linguagens suportadas

- Python
- Java
- PHP
- Node.js
- Go

---

### 🧩 Cloud Functions (FaaS / Serverless)

Ideal para pequenos eventos automatizados.

#### Exemplos:
- processar upload de imagens
- responder eventos HTTP
- executar automações

---

### 💰 Grande Benefício

Você paga apenas pelo tempo real de execução da função.

Cobrança:
- por milissegundos

---

## 💻 5. Automação e CLI: Cloud Shell e Gsutil

O verdadeiro poder da nuvem está na automação via terminal.

---

### ☁️ Cloud Shell

Terminal web pré-configurado pelo Google.

#### Já vem instalado:
- gcloud
- gsutil
- git

#### Benefícios:
- Segurança corporativa
- Ambiente isolado
- Sem instalação local

---

### 🛠️ Gsutil: Manipulação de Buckets

Ferramenta CLI para gerenciamento do Cloud Storage.

---

#### Criar Bucket

```bash
gsutil mb gs://nome-do-bucket
```

---

#### Enviar Arquivo

```bash
gsutil cp imagem.jpg gs://nome-do-bucket
```

---

#### Listar Arquivos

```bash
gsutil ls gs://nome-do-bucket
```

---

## 🚀 6. Deploy Completo em 3 Passos

Como publicar uma aplicação no App Engine sem gerenciar servidores.

---

### 📥 1. Preparar o Código

Clone ou envie os arquivos da aplicação para o Cloud Shell.

Exemplo:
- aplicação Flask em Python

---

### ⚡ 2. Deploy da Aplicação

```bash
gcloud app deploy
```

O Google automaticamente:
- provisiona infraestrutura
- configura balanceadores
- publica a aplicação
- escala conforme demanda

---

### 🌍 3. Aplicação no Ar

Após o deploy:
- uma URL pública é gerada
- a aplicação fica acessível globalmente

---

## 🧭 7. Conclusão

O GCP entrega flexibilidade total, indo da infraestrutura tradicional até computação totalmente serverless.

---

### ☁️ Principais Destaques

#### 🪣 Storage
Classes inteligentes de armazenamento para diferentes cenários.

#### 🖥️ Compute Engine (IaaS)
Controle total de hardware com acesso SSH simplificado.

#### ⚡ App Engine (PaaS)
Foco absoluto no código sem gerenciamento de servidores.

#### 🧩 Cloud Functions
Execução de pequenas funções sob demanda com cobrança por milissegundos.

---

### 🎁 Free Tier

O Google Cloud oferece:
- créditos iniciais (geralmente US$ 300)
- serviços gratuitos permanentes
- ambiente ideal para laboratórios e estudos

---

<br>

## 📚 8. Trilha

Para aprofundamento do conteúdo, acesse minha trilha de estudos na Alura:

<div align="center">

<a href="https://cursos.alura.com.br/fundamentos-e-administracao-cloud-computing-beatriz-camargo-serafini-1778537955469-p1080290">
  <img src="https://img.shields.io/badge/📖%20Acessar%20Trilha%20na%20Alura-cd9bcc?style=for-the-badge" />
</a>

</div>
