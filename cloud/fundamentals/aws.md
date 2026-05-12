<div align="center">

# ☁️ Amazon Web Services (AWS)

### Do Macro à Execução: A anatomia da nuvem líder mundial, da infraestrutura global à automação via CLI.

</div>

---

<br>

<table align="center" width="850" cellpadding="18" style="border-collapse: collapse; background-color:#f8f1f5; border-radius:14px;">

<tr>

<td>

## 🏆 1. Por que estudar AWS e o caminho das Certificações

A Amazon transformou a gigantesca infraestrutura que suportava seu e-commerce em um produto comercializável. Hoje, a AWS é a líder absoluta do mercado global de nuvem pública (com cerca de 1/3 do mercado), tornando profissionais especializados altamente valorizados.

Para quem está começando, o ponto de partida é a certificação **AWS Certified Cloud Practitioner (CCP)**.

#### O Mapa Completo de Certificações AWS
Embora a certificação Cloud Practitioner (CCP) seja a porta de entrada, a AWS possui um ecossistema completo de certificações divididas por níveis e funções. As principais trilhas incluem:

- Arquitetos: AWS Certified Solutions Architect (níveis Associate e Professional).
- Operações e Infraestrutura: AWS Certified SysOps Administrator (Associate) e AWS Certified DevOps Engineer (Professional).
- Desenvolvedores: AWS Certified Developer (Associate) e AWS Certified DevOps Engineer (Professional).
- Especialidades (Specialty): Certificações hiperfocadas, como Segurança (AWS Certified Security) ou até mesmo construção de habilidades para a Alexa (AWS Certified Alexa Skill Builder).

#### Detalhes extras sobre a prova CCP
- O Exame: Cerca de 65 perguntas (múltipla escolha/múltiplas respostas), duração de 90 minutos, custo médio de US$ 100. Pode ser feito presencialmente ou online (supervisionado no conforto da sua casa).
- Idioma: Disponível em diversos idiomas, inclusive português (embora o inglês seja muito comum).
- Público: Recomendado para quem tem no mínimo 6 meses de familiaridade com a AWS (engloba áreas técnicas, gerenciais e vendas).
- Habilidades Validadas: Compreensão da infraestrutura global, modelos de faturamento, principais serviços, modelo de segurança compartilhada, princípios de arquitetura e fontes de suporte técnico (whitepapers).

---

## 🌍 2. A Infraestrutura Global
A AWS funciona de forma descentralizada para garantir altíssima disponibilidade.

### 📍 Regiões (Regions)
São áreas geográficas isoladas (ex: sa-east-1 em São Paulo, operando desde 2011). Atualmente, existem mais de 30 regiões no mundo.

#### Importância:
- Escolher a região certa é vital para garantir baixa latência.
- Conformidade legal (ex: manter dados de clientes fisicamente no Brasil).

---

### 🏢 Zonas de Disponibilidade (AZs)
Cada região possui no mínimo 2 AZs (São Paulo possui 3).

#### Características:
- Uma AZ é composta por um ou mais data centers físicos distintos.
- Possuem energia e rede independentes.
- Redundância é a regra para Disaster Recovery (Recuperação de Desastres).

---

### 🌐 Edge Locations (Pontos de Borda)
Centenas de pontos espalhados pelo mundo que funcionam como cache para entregar conteúdo mais rápido aos usuários finais (usados pelo serviço Amazon CloudFront).

(O mapa interativo oficial, atualizado constantemente, pode ser visualizado em: https://www.infrastructure.aws/)
</td>

</tr>

</table>

---

<br>

## 🕹️ 3. O Espectro de Interação: Como acessar a AWS
Você pode gerenciar sua nuvem de três maneiras:

- AWS Management Console: O portal web com interface gráfica. Ideal para o primeiro contato, exploração visual e configurações manuais pontuais.
- AWS CLI (Command Line Interface): Acesso por linha de comando no terminal. Ideal para automação via scripts e criação de infraestruturas em massa.
- AWS SDK (Software Development Kit): Bibliotecas que permitem integrar os serviços da AWS diretamente no código das suas aplicações usando linguagens como Python (via biblioteca boto3), Java ou JavaScript.

---

<br>

## 💻 4. O Coração da Nuvem: Serviços Principais de Computação
A matriz de computadores da AWS se divide em diferentes níveis de controle e abstração:

- EC2 (Elastic Compute Cloud): IaaS puro. O carro-chefe da AWS. Permite alugar Máquinas Virtuais (VMs) Linux, Windows ou macOS altamente customizáveis.
- ECS (Elastic Container Service): Serviço altamente escalável e seguro para orquestração e gestão de containers Docker.
- Elastic Beanstalk: PaaS. Focado em deploy rápido. Você faz o upload do seu código e a AWS automatiza o provisionamento, balanceamento de carga e segurança.
- Lambda (Serverless / FaaS): Computação sem servidor. Você escreve trechos de código e a AWS roda automaticamente sob demanda, cobrando apenas pelos milissegundos de execução. Ideal para microsserviços.

---

<br>

## 🖥️ 5. Mergulho no EC2: Arquitetura e Modelos de Cobrança
Para provisionar um servidor EC2 via console de forma manual, você segue um roteiro base:

- AMI (Amazon Machine Image): Escolher o Sistema Operacional base.
- Tipo de Instância: Escolher o poder de fogo (capacidade de CPU e RAM).
- EBS (Elastic Block Store): Definir o disco rígido (SSD para performance ou HDD para armazenamento em massa).
- Security Group: Configurar o firewall (ex: abrir a porta 80 para web ou 22 para acesso remoto).
- Key Pair (Par de Chaves): Gerar um arquivo .pem para acessar o servidor de forma segura via SSH.
---

<br>

### 💰 Otimização Financeira: Modelos de Cobrança do EC2

| Modelo | Dinâmica | Uso Ideal e Exemplos Reais |
|---|---|---|
| Sob Demanda (On-Demand) | Pagamento por hora/segundo. Nenhuma fidelidade ou pagamento antecipado. | Picos sazonais (Black Friday) ou validação de novas ideias. Flexibilidade total. |
| Instâncias Reservadas | Contratos de 1 a 3 anos. Descontos agressivos de até 75%. | Aplicações sólidas com tráfego previsível a longo prazo (ex: banco de dados principal de um sistema de RH). |
| Instâncias Spot (Leilão) | Lances pela capacidade ociosa dos data centers. Custo baixíssimo, mas a AWS pode tomar a máquina de volta com 2 min de aviso. | Processamento em lote, renderização de vídeo 3D ou treinamento intenso de modelos de IA. |
| Dedicadas (Dedicated Hosts) | Servidor físico totalmente dedicado à sua empresa. | Requisitos rigorosos de conformidade legal ou licenciamento de software antigo atrelado ao hardware físico. |

---

<br>

## 🏗️ 6. Governança e Melhores Práticas
A verdadeira maestria em nuvem não é apenas saber criar um servidor, mas projetá-lo de forma otimizada e segura.

### 🔑 IAM (Identity and Access Management)
O centro de segurança da AWS.

- NUNCA use a conta "Root" (conta mestre) para o dia a dia.
- Você deve criar Usuários, agrupá-los em Grupos (ex: Devs, DBAs) e atribuir Políticas de acesso.
- Baseia-se no princípio do privilégio mínimo (ex: dar permissão de leitura, mas não de exclusão).
- É aqui que são geradas as chaves de acesso para usar a CLI.

---

### 🏛️ AWS Well-Architected Framework

Começou como um único documento em PDF (Whitepaper) e hoje evoluiu para um framework completo. É um manual de boas práticas vitais para evitar infraestruturas subdimensionadas ou superestimadas.

Para ajudar as empresas a medirem se estão seguindo as regras, a Amazon disponibiliza o AWS Well-Architected Tool, uma ferramenta prática de avaliação.

#### Os 6 Pilares:
- Excelência Operacional: Automatizar mudanças e responder a eventos diários.
- Segurança: Proteger informações, sistemas e rastrear acessos (KMS, IAM).
- Confiabilidade: A capacidade do sistema se recuperar rapidamente de falhas (Multi-AZ, Autoscaling).
- Eficiência de Performance: Usar recursos de TI de forma adaptável à demanda.
- Otimização de Custos: Pagar apenas pelo necessário, eliminando recursos ociosos.
- Sustentabilidade: Minimizar o impacto ambiental com eficiência energética.

---

### 🧠 Princípios de Arquitetura Inegociáveis

- Pare de adivinhar suas necessidades de capacidade: Na nuvem, graças à elasticidade, você usa apenas o necessário e dimensiona para cima ou para baixo automaticamente.
- Sistemas de teste na escala de produção: Crie um ambiente de teste idêntico ao real sob demanda, rode simulações de estresse e desative os recursos logo em seguida.
- Automatize para facilitar a experimentação: A automação permite criar, replicar e alterar cargas de trabalho a um baixo custo. Facilita reverter sistemas para parâmetros anteriores instantaneamente em caso de erro.
- Permita arquiteturas evolutivas: A arquitetura não é engessada; ela evolui continuamente para atender aos novos requisitos do negócio.
---

### 🛡️ Trusted Advisor (O Consultor Automatizado)
Ferramenta nativa que cruza a sua infraestrutura em uso com os 6 pilares do Well-Architected.

Ele fornece alertas em tempo real sobre:
- portas abertas (risco de segurança)
- instâncias EC2 ociosas gastando dinheiro à toa
- gargalos de performance

---

<br>


## ⚙️ 7. O Poder da Automação (AWS CLI)
Quando a arquitetura atinge maturidade, clicar em botões no console manual torna-se um gargalo ineficiente (é inviável ligar/desligar 100 servidores manualmente). A transição para a operação via CLI permite escalar instantaneamente, pavimentando o caminho para a Infraestrutura como Código (IaC).

### 🚀 Passo a passo para operar via CLI:
#### 1. Preparando o Terreno (No IAM):
- Criar um grupo (ex: CLI_Users) com a política adequada (ex: AmazonEC2FullAccess).
- Criar um usuário atrelado a esse grupo com acesso programático.
- A AWS gerará duas credenciais cruciais: Access Key ID e Secret Access Key.

#### 2. Autenticando o Terminal:
Com a CLI instalada no seu computador, inicie a configuração:
```bash
$ aws configure --profile meu_usuario_aws
AWS Access Key ID [None]: AKIAIOSFODNN7EXAMPLE
AWS Secret Access Key [None]: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
Default region name [None]: us-east-1
Default output format [None]: json
```
(Análise: Este comando vincula as chaves de segurança localmente, direciona os comandos para a região da Virgínia e define o formato de retorno visual como JSON).

#### 3. Visibilidade e Inventário:
```bash
$ aws ec2 describe-instances --profile meu_usuario_aws
```
(Este comando retorna um JSON enorme com todos os detalhes das suas instâncias. O dado mais importante a ser extraído aqui é o "InstanceId", que é o RG do seu servidor).

#### 4. Automação e Otimização (Ligando e Desligando):
Para cortar custos desligando a máquina no fim do expediente:
```bash
$ aws ec2 stop-instances --instance-ids i-087643300b1e20fa5 --profile meu_usuario_aws
```
Para religar a máquina no dia seguinte:
```bash
$ aws ec2 start-instances --instance-ids i-087643300b1e20fa5 --profile meu_usuario_aws
```
---

<br>

## 🧭 8. Conclusão: O Profissional do Futuro
A evolução na nuvem começa entendendo os data centers físicos, passa pela aplicação dos pilares do Well-Architected e atinge seu ápice na automação.

Dominar a AWS transcende operar painéis visuais: é a capacidade de tratar uma infraestrutura colossal com a agilidade, o versionamento e a eficiência típicos do desenvolvimento de software puro.
---

<br>

## 📚 10. Trilha

Para aprofundamento do conteúdo, acesse minha trilha de estudos na Alura:

<div align="center">

<a href="https://cursos.alura.com.br/fundamentos-e-administracao-cloud-computing-beatriz-camargo-serafini-1778537955469-p1080290">
  <img src="https://img.shields.io/badge/📖%20Acessar%20Trilha%20na%20Alura-cd9bcc?style=for-the-badge" />
</a>

</div>
