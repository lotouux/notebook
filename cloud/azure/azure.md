<div align="center">

# ☁️ Microsoft Azure

### O Paradigma da Nuvem, Arquitetura de Serviços, Máquinas Virtuais e Automação

</div>

---

<br>

<table align="center" width="850" cellpadding="18" style="border-collapse: collapse; background-color:#f8f1f5; border-radius:14px;">

<tr>

<td>

## 💡 1. O Paradigma da Nuvem: Datacenter Tradicional vs Azure

O Microsoft Azure é a plataforma de computação em nuvem da Microsoft, oferecendo uma alternativa moderna, flexível e escalável aos datacenters locais tradicionais.

---

### 🏢 Hardware Local (CapEx - Despesa de Capital)

- Responsabilidade total: Compra de servidores, manutenção física e refrigeração.
- Altíssimo custo inicial: O investimento é feito antes mesmo do projeto dar lucro.
- Risco: Superestimar ou subestimar a capacidade necessária.

---

### ☁️ Nuvem Azure (OpEx - Despesa Operacional)

- A Abstração: A Microsoft gerencia 100% da infraestrutura física.
- Sob demanda: O usuário aluga poder de computação, armazenamento e rede.
- Pay-as-you-go: Pagamento apenas pelo que utiliza, sem investimento inicial.

---

### 🎁 O Incentivo Gratuito

Para novos usuários, a Microsoft oferece cerca de US$ 200 (ou aprox. R$ 900) em créditos para explorar a plataforma, além de acesso gratuito a serviços populares por 12 meses e mais de 25 produtos sempre gratuitos.

---

## 🗺️ 2. O Mapa de Serviços do Azure

A plataforma é dividida em várias categorias. As principais são:

---

### 🖥️ Computação

- Máquinas Virtuais (VMs): IaaS puro (infraestrutura). Controle total do SO.
- App Services: PaaS para hospedagem de aplicações web sem gerenciar servidores.
- Serviços de Container (AKS): Orquestração de containers via Kubernetes.

---

### 💾 Dados e Armazenamento

- Azure Storage: Blob (arquivos em massa/imagens), Table (NoSQL), Files (compartilhamento de rede).
- Bancos de Dados: SQL Database (PaaS), Cosmos DB (NoSQL global), Redis Cache.

---

### 🌐 Redes e Identidade

- Redes Virtuais (VNets): Redes privadas isoladas na nuvem.
- Azure Active Directory (Azure AD / Entra ID): Gestão de identidade e controle de acesso.
- DNS e ExpressRoute: Gerenciamento de tráfego e conexão dedicada.

---

## ⚙️ 3. Foco Estratégico: Máquinas Virtuais (IaaS)

As VMs são a base da Infraestrutura como Serviço no Azure. Elas emulam um servidor físico na nuvem.

### 🎯 Controle Total

Diferente dos modelos PaaS, aqui o usuário é responsável pela instalação, configuração, manutenção de software e atualizações do Sistema Operacional (Windows ou Linux).

---

### 🚀 Casos de Uso (Exemplos Reais)

- Lift and Shift: Migração direta de datacenters locais para a nuvem sem reescrever o código do sistema.
- Sistemas Legados e Complexos: Servidores Oracle, SQL Server tradicionais ou controladores de domínio Active Directory.

---

## 💰 4. Faturamento e Estado da VM (Atenção aos Custos!)

A cobrança de computação das VMs é feita por minuto de uso. Entender os estados da máquina é fundamental para evitar desperdício financeiro.

| Estado | Funcionamento | Cobrança |
|---|---|---|
| 🟢 Running | VM ligada e operando normalmente | Você é cobrado |
| 🟡 Stopped | Sistema desligado, mas hardware reservado | Você continua sendo cobrado |
| 🔴 Deallocated | Hardware liberado para a Microsoft | Cobrança de computação interrompida |

---

### ⚠️ Atenção aos Discos

Independentemente da VM estar executando ou desalocada, você continuará pagando pelo armazenamento dos discos (VHDs), já que os dados permanecem guardados nos datacenters.

---

## 🏗️ 5. A Anatomia de uma VM no Azure

Para uma máquina virtual funcionar corretamente, ela depende de vários componentes de infraestrutura.

---

### 💽 Discos (VHDs)

Armazenados de forma durável via Azure Blob Storage.

- Disco do SO: Obrigatório. Contém Windows ou Linux.
- Disco Temporário: Armazenamento curto para paginação e cache.
- Discos de Dados: Opcionais para bancos de dados ou arquivos pesados.

⚠️ Atenção: Dados do disco temporário podem ser perdidos em reinicializações.

---

### 🌐 Rede Virtual (VNet) e Sub-redes

Sua VM precisa de um ambiente de rede para comunicação.

- Sub-rede (Subnet): Segmento isolado de IPs.
- Endereço IP Público: Acesso externo via internet.
- Endereço IP Privado: Comunicação interna segura.

---

### 🛡️ Network Security Group (NSG)

É o firewall da sua VM.

Ele controla tráfego de entrada e saída através de regras específicas:

- Porta 80 → HTTP
- Porta 3389 → RDP
- Porta 22 → SSH

---

## 🖥️ 6. Criação Visual: O Portal do Azure

O `portal.azure.com` é a interface gráfica centralizada da plataforma.

### 🚀 Passo a Passo da Implementação

#### 1. Projeto
- Criar ou selecionar um Grupo de Recursos.
- Exemplo: `servidores_win`

#### 2. Instância e Tamanho
- Definir região (ex: Brazil South).
- Escolher a imagem do sistema operacional.

#### 3. Autenticação
- Criar usuário administrador.
- Definir senha forte (mínimo 12 caracteres).

#### 4. Rede e NSG
- Liberar portas necessárias:
  - RDP (3389)
  - HTTP (80)

---

### ⚙️ Abas Adicionais

#### Gerenciamento
- Ativar Azure Security Center.
- Configurar Auto-shutdown.

#### Revisar + Criar
- Azure valida a configuração.
- Exibe custo estimado por hora.
- Inicia o deploy automaticamente.

---

## 🔌 7. Conexão Remota (Acessando seu Servidor)

Após criar a VM, é necessário acessar o sistema operacional remotamente.

---

### 🪟 Ambiente Windows (Via RDP)

1. Vá até a VM no portal Azure.
2. Clique em **Conectar**.
3. Baixe o arquivo `.rdp`.
4. Abra no seu computador.
5. Informe usuário e senha.

✅ Resultado: acesso gráfico completo ao Windows Server.

---

### 🐧 Ambiente Linux (Via SSH)

1. Descubra o IP público da VM.
2. Abra o terminal.
3. Execute:

```bash
ssh usuario@ip_da_maquina
```

4. Informe a senha.

✅ Resultado: acesso remoto via terminal Linux.

---

## ⚡ 8. A Alternativa Ágil: Azure Cloud Shell e Automação

O Azure Cloud Shell (`shell.azure.com`) fornece um terminal web com Azure CLI já configurada.

---

### 🚀 Criando Infraestrutura via CLI

#### 1. Criando o Grupo de Recursos

```bash
az group create --name vm-grupo --location brazilsouth
```

---

#### 2. Criando a Máquina Virtual

```bash
az vm create \
  --resource-group vm-grupo \
  --name LinuxVM \
  --image UbuntuLTS \
  --admin-username admin123 \
  --admin-password Admin123@ \
  --location brazilsouth
```

Resultado:
- VM criada
- IP público provisionado
- Status `VM running`

---

### 📝 Cheat Sheet: Gestão da VM via CLI

| Comando | Objetivo |
|---|---|
| `az vm list-ip-addresses` | Descobrir IPs da VM |
| `az vm deallocate` | Desalocar VM e parar cobrança |
| `az vm start` | Ligar VM novamente |
| `az vm delete` | Excluir apenas a VM |
| `az group delete --name vm-grupo` | Remover toda infraestrutura |

---

## 🔬 9. O Propósito: Cenários Dev/Test e Controle Financeiro

A nuvem revolucionou ambientes de desenvolvimento e testes.

---

### 🚀 Isolamento Ágil e Descarte

Antes:
- Empresas compravam servidores físicos caros.
- Infraestrutura ficava ociosa após testes.

Com Azure:
- Criação de ambientes idênticos à produção em minutos.
- Testes isolados e temporários.
- Destruição completa do ambiente após uso.

---

### 🛡️ Proteção de Orçamento (Auto-shutdown)

Configure sempre o desligamento automático da VM.

Exemplo:
- Desligar automaticamente às 19h00.
- Evita desperdício financeiro com recursos esquecidos ligados.

---

## 🧭 10. Conclusão

O Azure transforma infraestrutura tradicional em serviços elásticos, automatizados e escaláveis.

O verdadeiro diferencial da computação em nuvem não é apenas criar máquinas virtuais, mas automatizar ambientes inteiros, reduzir desperdícios e tratar infraestrutura com a mesma agilidade do desenvolvimento de software moderno.

---

<br>

## 📚 11. Trilha

Para aprofundamento do conteúdo, acesse minha trilha de estudos na Alura:

<div align="center">

<a href="#">
  <img src="https://img.shields.io/badge/📖%20Acessar%20Trilha%20na%20Alura-cd9bcc?style=for-the-badge" />
</a>

</div>
