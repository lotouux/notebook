<div align="center">

# ♾️ Cultura DevOps e DevSecOps

### O Fim dos Silos: Automação, Entrega Contínua e Segurança Deslocada à Esquerda.

</div>

---

<br>

<table align="center" width="850" cellpadding="18" style="border-collapse: collapse; background-color:#f8f1f5; border-radius:14px;">

<tr>

<td>

## ⚔️ 1. O Paradoxo Tradicional da TI e a "Parede de Confusão"

Em empresas tradicionais, a TI costuma ser separada em dois mundos com objetivos completamente diferentes, criando o famoso conflito entre desenvolvimento e operações.

### 💻 Equipe de Desenvolvimento (Dev)
A missão da equipe Dev é:

- Criar funcionalidades rapidamente.
- Entregar inovação contínua.
- Alterar o código constantemente.
- Acelerar releases.

#### Objetivo:
Mudança e velocidade.

---

### 🖥️ Equipe de Operações (Ops)
A equipe Ops é responsável por:

- Garantir estabilidade.
- Evitar falhas em produção.
- Manter sistemas disponíveis.
- Reduzir riscos operacionais.

#### Objetivo:
Controle e estabilidade.

---

### 🚧 O Problema: A "Parede de Confusão"

Enquanto os Devs querem mudar tudo rapidamente, Ops tenta impedir mudanças perigosas.

Resultado:
- Lentidão em entregas.
- Conflitos internos.
- Deploys arriscados.
- Ambientes inconsistentes.
- Cultura de culpa.

---

### 🤝 A Solução: Cultura DevOps

DevOps não é uma ferramenta.

É uma cultura organizacional criada para eliminar os silos entre desenvolvimento e operações.

#### O objetivo:
Entregar software com:
- velocidade
- automação
- estabilidade
- segurança
- escalabilidade

---

### 🧠 O que muda no modelo DevOps?

- Desenvolvedores ganham autonomia sobre infraestrutura.
- SysAdmins participam desde o planejamento.
- Automação substitui processos manuais.
- Toda a equipe compartilha responsabilidade ponta a ponta.

Isso cria o famoso:
#### 🔥 Ownership (Sentimento de Dono)

</td>

</tr>

</table>

---

<br>

## 🚀 2. O Motor DevOps: Ganhos Estratégicos

A quebra da "Parede de Confusão" gera benefícios técnicos e estratégicos extremamente relevantes.

### ⚡ Velocidade e Frequência de Entregas
- Releases menores e contínuos.
- Correções rápidas.
- Feedback acelerado.
- Time-to-market reduzido.

---

### 📈 Escalabilidade Inteligente
A infraestrutura passa a crescer automaticamente conforme a demanda.

Exemplo:
- aumento automático de servidores
- balanceamento de carga
- provisionamento via código

---

### 🛡️ Confiabilidade
A qualidade deixa de depender apenas de validação manual.

Entram em cena:
- testes automatizados
- pipelines
- monitoramento contínuo
- rollback automatizado

---

### 🤝 Colaboração Contínua
O modelo DevOps elimina a mentalidade:

> "isso não é problema meu"

Todos compartilham:
- responsabilidade
- métricas
- estabilidade
- qualidade do produto

---

<br>

## 🏗️ 3. Os 3 Pilares da Automação DevOps

A cultura DevOps depende de três práticas técnicas fundamentais.

---

### 📜 1. Infraestrutura como Código (IaC)

Em vez de configurar servidores clicando manualmente em painéis, toda a infraestrutura é criada através de código.

#### Benefícios:
- Versionamento
- Ambientes reproduzíveis
- Provisionamento automático
- Padronização
- Redução de erros humanos

#### Exemplos:
- Terraform
- CloudFormation
- Ansible

---

### 🧩 2. Arquitetura de Microsserviços

O software deixa de ser um grande bloco monolítico.

Agora ele é dividido em pequenos serviços independentes.

#### Vantagens:
- Escalabilidade individual
- Deploy isolado
- Resiliência
- Facilidade de manutenção

---

### 🔄 3. CI/CD (Integração e Entrega Contínuas)

#### CI — Continuous Integration
Sempre que um desenvolvedor envia código:

- testes automatizados executam
- validações acontecem
- erros são detectados cedo

---

#### CD — Continuous Delivery / Deployment
Após aprovação:

- o software é empacotado
- validado
- preparado automaticamente para produção

Tudo isso com mínima intervenção humana.

---

<br>

## ♾️ 4. O Circuito Infinito: O Ciclo de Vida DevOps

O DevOps funciona como um fluxo contínuo de automação e melhoria.

---

### 📋 1. Planejamento (Plan)

Equipes organizam:
- backlog
- sprints
- estimativas
- prioridades

#### Ferramentas:
- Jira Software
- Trello
- Azure Boards

---

### 💻 2. Codificação (Code)

Desenvolvimento colaborativo do software e da infraestrutura.

#### Ferramentas:
- Git
- GitHub
- GitLab
- Confluence

---

### 🛠️ 3. Construção (Build)

O código é compilado e dependências são organizadas.

#### Ferramentas:
- Maven
- Gradle
- npm

Se houver erro de sintaxe:
- o pipeline falha imediatamente.

---

### 🧪 4. Validação (Test)

Execução automática de testes.

#### Tipos:
- testes unitários
- integração
- regressão
- testes de interface

#### Ferramentas:
- JUnit
- Selenium
- Cypress

---

### 📦 5. Release e Deploy

O software aprovado segue automaticamente para produção.

#### Ferramentas:
- Jenkins
- GitHub Actions
- GitLab CI/CD
- Docker

---

### ⚙️ 6. Operação e Monitoramento

A aplicação entra em produção sob observabilidade contínua.

#### Ferramentas:
- Kubernetes
- Ansible
- Datadog
- Splunk
- Nagios
- Prometheus

---

<br>

## 🛡️ 5. DevSecOps e o Paradigma Invertido da Segurança

No modelo tradicional:

- a segurança era validada apenas no final.
- falhas graves eram descobertas tarde.
- correções custavam caro.

---

### 🔄 A Evolução: Shifting Security Left

O mercado adotou o conceito:

## ⬅️ Shift Left Security

Isso significa:
- mover segurança para o início do desenvolvimento.

A segurança deixa de ser uma etapa final e passa a existir desde:
- planejamento
- codificação
- build
- testes

---

### 🔐 O que o DevSecOps garante?

#### Segurança Distribuída
Toda a equipe compartilha responsabilidade pela proteção do sistema.

---

#### Prevenção Antecipada
Falhas são detectadas antes do deploy.

---

#### Redução de Custos
Corrigir uma vulnerabilidade:
- no código → barato
- em produção → extremamente caro

---

### 🧠 Ferramentas comuns de DevSecOps

| Categoria | Ferramentas |
|---|---|
| SAST | SonarQube, Checkmarx |
| Segurança de Containers | Trivy, Clair |
| Gestão de Segredos | Vault |
| Monitoramento | Falco |
| Dependências Vulneráveis | Snyk |

---

<br>

## 🧭 6. Conclusão: A Síntese do Ecossistema

DevOps e DevSecOps representam uma transformação cultural profunda.

Não são apenas cargos ou ferramentas.

São modelos operacionais completos onde:

- automação substitui tarefas manuais
- equipes trabalham de forma integrada
- segurança nasce junto com o software
- mudanças acontecem continuamente

O resultado é um ecossistema capaz de entregar:
- inovação rápida
- alta disponibilidade
- confiabilidade
- segurança
- escalabilidade

Tudo isso sustentado por pipelines automatizados e infraestrutura programável.

---

<br>

## 📚 7. Trilha

Para aprofundamento do conteúdo, acesse minha trilha de estudos na Alura:

<div align="center">

<a href="https://cursos.alura.com.br/fundamentos-e-administracao-cloud-computing-beatriz-camargo-serafini-1778537955469-p1080290">
  <img src="https://img.shields.io/badge/📖%20Acessar%20Trilha%20na%20Alura-cd9bcc?style=for-the-badge" />
</a>

</div>
