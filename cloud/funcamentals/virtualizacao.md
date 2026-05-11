<div align="center">

# ☁️ Virtualização

### Infraestrutura, abstração de hardware e segurança na computação moderna

</div>

---

<br>

<table align="center" width="850" cellpadding="18" style="border-collapse: collapse; background-color:#f8f1f5; border-radius:14px;">

<tr>

<td>

## 🌐 1. O que é Virtualização

Antigamente, sistemas operacionais estavam diretamente ligados ao hardware físico. Para melhorar performance, era necessário realizar upgrades físicos (upgrade vertical), o que gerava custo e limitação.

A virtualização surge como solução através da **abstração de hardware**, permitindo que recursos físicos sejam compartilhados e distribuídos de forma dinâmica.

Com isso, nasce o conceito de **clusters**, onde múltiplas máquinas físicas trabalham juntas como uma única infraestrutura lógica (upgrade horizontal), permitindo:

- Escalabilidade
- Alta disponibilidade
- Balanceamento de carga
- Expansão sob demanda com VMs

</td>

</tr>

</table>

---

<br>

## 🧱 2. Arquitetura da Virtualização

A virtualização é composta por três camadas principais:

### 🖥️ Host (Hospedeiro)
Infraestrutura física real (CPU, RAM, disco).

### ⚙️ Hypervisor
Camada de software responsável por abstrair e distribuir os recursos físicos.

### 💻 Guest (Máquina Virtual)
Sistemas operacionais virtuais que rodam sobre o hypervisor.

Exemplo: múltiplas VMs em um único servidor físico (App, DB, Web etc).

---

<br>

## 🧩 3. SDDC — Software-Defined Data Center

A virtualização evolui para o conceito de data centers totalmente definidos por software:

- **Compute (VMs):** CPU e RAM virtualizados
- **Storage (SDS):** armazenamento em pools lógicos
- **Network (SDN):** redes configuráveis via software

Tudo passa a ser programável, elástico e automatizável.

---

<br>

## ⚡ 4. Benefícios da Virtualização

- Redução de custos operacionais
- Melhor aproveitamento de hardware
- Gerenciamento centralizado
- Execução simultânea de múltiplos serviços
- Suporte a sistemas legados
- Isolamento entre ambientes (segurança)

---

<br>

## 🧠 5. Tipos de Virtualização

### 🖥️ Virtualização de Aplicações
Aplicações executadas remotamente e transmitidas ao usuário.

Exemplo: cloud gaming.

---

### 🧱 Máquinas Virtuais (VMs)
- Sistema operacional completo por instância
- Alto isolamento
- Maior consumo de recursos
- Inicialização mais lenta

---

### ⚡ Containers
- Compartilham o kernel do sistema host
- Leves e rápidos
- Inicialização em segundos
- Ideais para microsserviços

---

### 📊 Comparativo

| Característica | VM | Container |
|----------------|----|----------|
| Abstração | Hardware | Sistema Operacional |
| Peso | Alto | Baixo |
| Boot | Lento | Rápido |
| Isolamento | Alto | Moderado |
| Uso ideal | Sistemas legados | Microsserviços |

---

<br>

## ⚙️ 6. Hypervisores

### Tipo 1 (Bare Metal)
- Instalado diretamente no hardware
- Usado em data centers
- Alta performance
- Ex: VMware ESXi

### Tipo 2 (Hosted)
- Instalado sobre um sistema operacional
- Usado para testes locais
- Ex: VirtualBox

---

### 🔎 Virtualização Total vs Paravirtualização

**Virtualização Total**
- Sistema convidado não sabe que é virtual
- Mais compatibilidade
- Menor performance

**Paravirtualização**
- Sistema convidado “sabe” que é virtual
- Menos overhead
- Maior performance em I/O

---

<br>

## 🔐 7. Virtualização e Segurança Cibernética

A virtualização é fundamental para segurança e análise de sistemas.

### 🧪 Sandboxes
Ambientes isolados usados para executar malware sem risco ao sistema real.

---

### 🌐 Topologias de Rede

- **Host-only:** rede isolada (máxima segurança)
- **NAT:** acesso à internet com IP mascarado
- **Bridged:** VM visível como máquina real na rede

---

### 🛡️ Boas práticas

- Snapshots para restauração rápida
- Pastas compartilhadas em modo somente leitura
- Atualização constante do hypervisor
- Isolamento rigoroso de ambientes de teste

---

<br>

## 🧭 8. Conclusão

A virtualização é a base da computação moderna e da nuvem.

Ela permite escalabilidade, segurança, eficiência e automação em larga escala.

Dominar seus conceitos é essencial para qualquer área de infraestrutura, cloud e DevOps.

</div>
