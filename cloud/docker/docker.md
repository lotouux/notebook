<div align="center">

# 🐳 Docker e Containers

### O Fim do Monolito: Virtualização Leve, DevOps e a Arquitetura de Microsserviços

</div>

---

<br>

<table align="center" width="850" cellpadding="18" style="border-collapse: collapse; background-color:#f8f1f5; border-radius:14px;">

<tr>

<td>

## 💡 1. Ponto de Virada: Máquinas Virtuais vs Containers

A evolução da infraestrutura passou dos clusters físicos para as Máquinas Virtuais (VMs), até chegar aos Containers: leves, rápidos e altamente portáveis.

---

### 🖥️ Máquinas Virtuais (Hardware-Based)

A virtualização baseada em hardware exige um Sistema Operacional completo para cada VM.

#### Características:
- Sistema Operacional isolado
- Kernel próprio
- Alto consumo de recursos
- Inicialização lenta

#### Impactos:
- Peso em Gigabytes
- Boot em minutos
- Memória reservada pelo hypervisor

---

### 🐳 Containers (OS-Based)

Containers compartilham o kernel do sistema hospedeiro e executam aplicações como processos isolados.

#### Características:
- Compartilhamento de kernel
- Inicialização extremamente rápida
- Muito mais leves

#### Benefícios:
- Peso em Megabytes
- Boot em milissegundos
- Melhor aproveitamento de hardware
- Execução quase nativa

---

## 🧩 2. A Essência do Docker e Seus Componentes

Criado em 2013, o Docker popularizou a virtualização por containers.

Sua filosofia:
> **Build, Ship, Run**

A proposta é empacotar código, dependências e configurações em um ambiente portátil e reproduzível.

---

## 🏗️ A Anatomia do Docker

### 📄 Dockerfile (A Receita)

Arquivo de texto contendo instruções para construção da imagem.

Exemplo:
```Dockerfile
FROM ubuntu
RUN apt-get update
```

---

### 📦 Docker Image (O Molde)

Template imutável contendo:
- bibliotecas
- dependências
- código-fonte
- configurações

---

### 🚀 Docker Container (Execução)

Instância prática de uma imagem sendo executada.

É:
- isolado
- portátil
- descartável

---

### ☁️ Docker Registry

Repositório de imagens Docker.

O principal:
- Docker Hub

Funciona como um GitHub de imagens.

---

### ⚙️ Docker Daemon

O motor responsável por:
- executar containers
- gerenciar imagens
- controlar volumes e redes

---

## ⚙️ 3. Sob o Capô: Como o Isolamento Funciona?

Containers não são Máquinas Virtuais completas.

Eles usam recursos nativos do kernel Linux para criar isolamento seguro.

---

### 🧩 Namespaces

Responsáveis pelo isolamento de:
- processos
- rede
- sistema de arquivos
- usuários

O container "acha" que está sozinho no sistema.

---

### 📊 Cgroups (Control Groups)

Controlam:
- CPU
- memória
- disco
- recursos de hardware

Evita que um container monopolize o servidor.

---

### 🔒 Chroot

Limita o diretório raiz visível para o container.

Cria uma espécie de "prisão" de arquivos.

---

## 🏗️ 4. O Fim do Monolito: Microsserviços

O Docker impulsionou fortemente a arquitetura moderna baseada em microsserviços.

---

### 🧱 Arquitetura Monolítica

Aplicação única:
- um código
- um deploy
- um serviço gigante

#### Problemas:
- difícil escalabilidade
- manutenção complexa
- falha em um módulo pode derrubar tudo

---

### 🧩 Arquitetura de Microsserviços

Cada funcionalidade roda isoladamente em containers independentes.

#### Benefícios:
- deploy isolado
- escalabilidade granular
- manutenção simplificada
- tolerância a falhas

---

### 🚀 Exemplo Real

Na Black Friday:
- escalar apenas o container do carrinho
- manter o restante do sistema intacto

---

## 🗂️ 5. Layers e Persistência de Dados

O Docker usa um sistema inteligente baseado em camadas.

---

### 🧱 Layers (Camadas)

Cada instrução do Dockerfile gera uma nova camada.

#### Características:
- somente leitura
- reutilizáveis
- compartilháveis

Resultado:
- economia de espaço
- builds mais rápidos

---

### ✍️ Copy-on-Write

Quando o container inicia:
- uma camada gravável é criada

Tudo acontece nela:
- logs
- arquivos
- alterações

---

### ⚠️ O Grande Risco

Se o container for destruído:
- todos os dados da camada gravável desaparecem.

---

## 💾 Volumes: Persistência Real

Volumes existem fora do ciclo de vida do container.

### Benefícios:
- persistência de dados
- backups simplificados
- compartilhamento entre containers
- segurança para bancos de dados

---

## 🎼 6. Docker Compose: Orquestrando Containers

Aplicações reais precisam de múltiplos containers:
- front-end
- back-end
- banco de dados
- cache

Gerenciar isso manualmente é inviável.

---

### ⚙️ Docker Compose

Ferramenta para subir ambientes completos usando um único arquivo YAML.

Arquivo padrão:
```yaml
docker-compose.yml
```

---

### 📦 Exemplo Conceitual

```yaml
version: "3"

services:
  app:
    image: nginx

  database:
    image: postgres
```

---

### 🚀 Comando Principal

```bash
docker-compose up
```

Resultado:
- toda infraestrutura sobe automaticamente.

---

## 🔄 7. Docker e a Cultura DevOps (CI/CD)

O Docker revolucionou pipelines modernos.

A grande vantagem:
- o mesmo container roda em qualquer ambiente.

---

### 🔁 Fluxo DevOps

1. Desenvolvedor cria container localmente
2. Pipeline CI/CD testa automaticamente
3. Produção recebe exatamente a mesma imagem

---

### 🎯 Benefícios

- redução de conflitos
- rollback rápido
- deploy previsível
- padronização de ambientes

---

## ☁️ 8. O Ecossistema da Nuvem Moderna

Arquiteturas modernas combinam múltiplos paradigmas.

---

### 🌍 The Edge (CDN)

Redes distribuídas globalmente:
- cache
- performance
- proteção DDoS

---

### 🐳 The Core Engine (Containers)

Docker atua como núcleo principal:
- APIs
- microsserviços
- processamento de negócio

---

### ⚡ The Event Horizon (Serverless)

Execução orientada a eventos:
- AWS Lambda
- Google Cloud Functions

#### Características:
- escala automática
- cobrança por execução
- infraestrutura invisível

---

## 🧭 9. Conclusão

O Docker redefiniu a forma como aplicações modernas são construídas e distribuídas.

Containers trouxeram:
- portabilidade
- velocidade
- isolamento
- automação
- escalabilidade

Hoje, dominar Docker significa entender a base operacional da computação em nuvem moderna, DevOps e arquiteturas distribuídas.

---

<br>

## 📚 10. Trilha

Para aprofundamento do conteúdo, acesse minha trilha de estudos na Alura:

<div align="center">

<a href="https://cursos.alura.com.br/fundamentos-e-administracao-cloud-computing-beatriz-camargo-serafini-1778537955469-p1080290">
  <img src="https://img.shields.io/badge/📖%20Acessar%20Trilha%20na%20Alura-cd9bcc?style=for-the-badge" />
</a>

</div>
