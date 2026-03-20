# google-cybersecurity-portfolio
Análise de riscos e conformidade (PCI DSS, GDPR, SOC) para a Botium Toys, desenvolvida durante a Certificação Profissional de Cibersegurança do Google.
# Projeto de Auditoria de Segurança: Botium Toys

Este projeto foi desenvolvido como parte do **Certificado Profissional de Cibersegurança do Google**, em parceria com o **CIEE**. O objetivo é aplicar na prática os conceitos de auditoria, gestão de riscos e conformidade (compliance) em um cenário empresarial real.

---

## 📚 Fundamentos: Categorias de Controle

Para esta análise, os controles de segurança foram classificados em três categorias principais, seguindo as melhores práticas do setor (NIST CSF):

1.  **Controles Administrativos/Gerenciais:** Políticas e procedimentos que definem como a organização gerencia dados e as responsabilidades dos funcionários (ex: Treinamentos, Políticas de Senha).
2.  **Controles Técnicos:** Soluções de hardware e software para proteger sistemas e redes (ex: Firewalls, Antivírus, Criptografia).
3.  **Controles Físicos/Operacionais:** Barreiras tangíveis que limitam o acesso físico a ativos (ex: Trancas, Câmeras CCTV, Sistemas de Incêndio).

---

## 🏢 Relatório de Avaliação de Risco (Botium Toys)

### Escopo e Objetivos
* **Escopo:** Revisão completa do programa de segurança, incluindo dispositivos de funcionários, rede interna e sistemas de e-commerce.
* **Objetivo:** Identificar lacunas de segurança e avaliar a conformidade com padrões globais para fortalecer a postura de segurança da empresa.

### Ativos Gerenciados
* Dispositivos de usuários finais (Laptops, Smartphones).
* Sistemas de inventário e bancos de dados.
* Infraestrutura de rede interna e acesso à internet.
* Produtos em estoque e manutenção de sistemas legados.

### Diagnóstico de Risco
* **Pontuação de Risco:** 8/10 (Alta).
* **Principais Descobertas:** Gerenciamento inadequado de ativos, ausência de criptografia em dados sensíveis e permissões de acesso excessivas para funcionários (exposição de dados de cartões de crédito).

---

## 📝 Checklist de Controles e Conformidade

Abaixo, apresento a auditoria detalhada baseada no cenário atual da organização.

### 1. Avaliação de Controles (Controls Assessment)

| Controle | Implementado | Categoria | Tipo |
| :--- | :---: | :--- | :--- |
| **Least Privilege** (Privilégio Mínimo) | ❌ No | Administrativo | Preventivo |
| **Disaster recovery plans** | ❌ No | Administrativo | Corretivo |
| **Password policies** | ✅ Yes | Administrativo | Preventivo |
| **Separation of duties** | ❌ No | Administrativo | Preventivo |
| **Firewall** | ✅ Yes | Técnico | Preventivo |
| **Intrusion detection system (IDS)** | ❌ No | Técnico | Detetivo |
| **Backups** | ❌ No | Técnico | Corretivo |
| **Antivirus software** | ✅ Yes | Técnico | Preventivo |
| **Manual monitoring (Legacy systems)** | ✅ Yes | Técnico | Preventivo |
| **Encryption** | ❌ No | Técnico | Dissuasivo |
| **Password management system** | ❌ No | Técnico | Preventivo |
| **Locks** (Escritórios, loja, armazém) | ✅ Yes | Físico | Preventivo |
| **CCTV surveillance** | ✅ Yes | Físico | Detetivo |
| **Fire detection/prevention** | ✅ Yes | Físico | Preventivo/Detetivo |

### 2. Checklist de Conformidade (Compliance)

#### **PCI DSS (Cartões de Pagamento)**
* **Acesso restrito apenas a usuários autorizados:** ❌ No
* **Dados armazenados/transmitidos em ambiente seguro:** ❌ No
* **Implementação de procedimentos de criptografia:** ❌ No
* **Adoção de políticas de gerenciamento de senhas seguras:** ❌ No

#### **GDPR (Proteção de Dados - UE)**
* **Dados de clientes da UE mantidos privados/seguros:** ❌ No
* **Plano de notificação de violação em até 72 horas:** ✅ Yes
* **Classificação e inventário adequado de dados:** ❌ No
* **Aplicação de políticas e processos de privacidade:** ✅ Yes

#### **SOC (Controles de Sistema e Organização)**
* **Políticas de acesso de usuário estabelecidas:** ❌ No
* **Confidencialidade de dados sensíveis (PII/SPII):** ❌ No
* **Integridade dos dados (consistência e precisão):** ✅ Yes
* **Disponibilidade de dados para usuários autorizados:** ✅ Yes

---

## 🚀 Recomendações Estratégicas

Com base nos riscos identificados, as seguintes medidas são recomendadas para mitigação imediata:

1. **Implementação de Criptografia:** Prioridade crítica para proteger dados de cartões de crédito, tanto em trânsito quanto em repouso (*at rest*), garantindo conformidade com o PCI DSS.
2. **Controle de Acesso (Privilégio Mínimo):** Reestruturar permissões de sistema para que os funcionários acessem estritamente o necessário para suas funções.
3. **Estratégia de Backup e Recuperação:** Implementar rotinas automatizadas de backup e um plano formal de recuperação de desastres (DRP) para garantir a continuidade do negócio em caso de incidentes.
4. **Sistema de Detecção de Intrusão (IDS):** Instalar ferramentas de monitoramento de rede para identificar tentativas de invasão e atividades maliciosas em tempo real.
