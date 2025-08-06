# GRC Notes (Governança, Riscos e Conformidade)

## Visão Geral
Este repositório reúne todos os meus estudos, anotações e referências relacionados à área de **GRC (Governança, Riscos e Conformidade)** dentro da cibersegurança. A ideia é construir um material de consulta e estudo que una teoria e prática sobre conformidade, gestão de riscos e estrutura de governança.

---

### Por que estudar GRC?
* Aumenta a maturidade de segurança de uma organização.
* Alinha os objetivos de segurança aos objetivos de negócio.
* Fortalece a reputação institucional e reduz riscos legais.
* Essencial para atuação como consultor, analista de risco ou auditor.

### Temas que serão abordados
* **ISO 27001**, **ISO 27005**
* **NIST Cybersecurity Framework**
* **LGPD**, **GDPR** e leis correlatas
* Gestão de riscos cibernéticos
* Auditorias internas e externas
* Conformidade e políticas de segurança
* Ferramentas GRC (RSA Archer, OneTrust, etc)

### Benefícios da documentação
* Consolidar conhecimento para certificações como **CRISC**, **CISA**.
* Facilitar revisões rápidas antes de auditorias.
* Criar referência prática para aplicação em projetos reais.

---

**Status**: Conteúdo em construção. Os tópicos serão adicionados conforme avanço nos estudos e projetos práticos da área.

# Projeto: Implementação de um Framework de Gerenciamento de Riscos Cibernéticos

## Visão Geral do Projeto
Este projeto documenta a aplicação prática de um framework de **Governança, Riscos e Conformidade (GRC)** para uma empresa fictícia, com o objetivo de identificar, avaliar e mitigar riscos cibernéticos. O foco é demonstrar uma abordagem estruturada e profissional para a gestão da segurança da informação, alinhando as estratégias de segurança aos objetivos de negócio.

Para este exercício, utilizaremos o **NIST Cybersecurity Framework (CSF)** como metodologia principal, devido à sua flexibilidade e ampla aceitação no mercado.

---

## Cenário da Empresa Fictícia
**Nome:** SecurTech Solutions
**Atividade:** Startup de Software-as-a-Service (SaaS) que oferece uma plataforma de gerenciamento de projetos para pequenas e médias empresas (PMEs).
**Tecnologia:** Infraestrutura hospedada na nuvem (AWS), utilizando containers Docker e Kubernetes. O sistema armazena dados de clientes, como informações de contato, dados de projetos e arquivos de negócios.
**Equipe:** 50 funcionários, incluindo equipes de desenvolvimento, vendas, suporte e liderança.

**Ativos Críticos:**
* Dados de Clientes (Confidencialidade e Disponibilidade são primordiais)
* Código-fonte da Plataforma (Integridade e Confidencialidade)
* Infraestrutura de Nuvem (Disponibilidade e Confidencialidade)
* Rede Interna da SecurTech (Integridade e Disponibilidade)

---

## Metodologia de Análise de Riscos (Baseada no NIST CSF)
O projeto será dividido nas cinco funções centrais do NIST CSF: **Identificar, Proteger, Detectar, Responder e Recuperar**. Cada função representa um ciclo de vida da segurança cibernética, e sua documentação demonstra um plano de segurança holístico.

### Fase 1: Identificar (Identify)
Nesta fase, o objetivo é desenvolver uma compreensão dos riscos de segurança cibernética para gerenciar os riscos para sistemas, ativos, dados e recursos da empresa.

**Tabela de Inventário de Ativos Críticos e Ameaças**

| Ativo Crítico         | Proprietário                 | Classificação    | Ameaças                                   |
|-----------------------|------------------------------|------------------|-------------------------------------------|
| Dados de Clientes     | Equipe de Cibersegurança     | Confidencial     | Vazamento de Dados, Ransomware, DDoS, Phishing |
| Código-fonte da Plataforma | Equipe de Desenvolvimento | Crítico          | Roubo de Propriedade Intelectual, Indisponibilidade |
| Infraestrutura de Nuvem | Equipe de Infra/DevOps       | Crítico          | Invasão, DDoS, Má Configuração             |
| Equipamentos de Funcionários | Equipe de TI               | Normal           | Phishing, Malware, Acesso Não Autorizado     |


<img width="800" height="1536" alt="image" src="https://github.com/user-attachments/assets/c9fb4831-63af-4087-bd07-8aef43b4c4ef" />


### Fase 2: Proteger (Protect)
Com base nos riscos identificados, esta fase foca na implementação de salvaguardas para garantir a entrega de serviços críticos de forma contínua.

**Controles de Proteção e Políticas de Segurança:**
* **Controle de Acesso:** Implementação de **Autenticação de Múltiplos Fatores (MFA)** para acesso a sistemas críticos e VPN. Uso do **Princípio do Mínimo Privilégio** para todos os funcionários.
* **Conscientização e Treinamento:** Programa obrigatório de treinamento em segurança para todos os funcionários, com simulações de **phishing** trimestrais.
* **Proteção de Dados:** Criptografia de dados **em trânsito** e **em repouso**. Políticas de backup e recuperação de dados.
* **Manutenção:** Gerenciamento de vulnerabilidades com escaneamento quinzenal. Aplicação de patches em sistemas operacionais e aplicações.

### Fase 3: Detectar (Detect)
Esta fase estabelece as atividades necessárias para identificar a ocorrência de um evento de segurança cibernética.

**Mecanismos de Detecção:**
* **Monitoramento Contínuo:** Implementação de um **SIEM (Security Information and Event Management)** para coletar e analisar logs de servidores, firewalls e endpoints.
* **Detecção de Intrusões:** Uso de um **IDS/IPS (Intrusion Detection/Prevention System)** para monitorar tráfego de rede em busca de atividades maliciosas.
* **Análise de Logs:** Rotina de análise de logs de acesso e eventos de segurança para identificar anomalias e tentativas de ataque.

### Fase 4: Responder (Respond)
Nesta fase, o foco é em como agir rapidamente após um incidente de segurança.

<img width="1024" height="1536" alt="image" src="https://github.com/user-attachments/assets/ce527795-129c-4d05-b84b-946ca37e3d59" />

### Fase 5: Recuperar (Recover)
Esta fase visa restaurar os serviços e operações que foram impactados por um incidente de segurança cibernética.

**Ações de Recuperação:**
* **Plano de Recuperação de Desastres (DRP):** Teste semestral do DRP para garantir que a SecurTech possa restaurar suas operações a partir de backups em caso de falha total.
* **Comunicação:** Plano de comunicação de crise para notificar clientes, parceiros e autoridades reguladoras (conforme LGPD e GDPR).
* **Melhoria Contínua:** Implementação das lições aprendidas de incidentes anteriores para fortalecer os controles de segurança existentes.

---

## Conclusão
A aplicação do framework NIST CSF na SecurTech Solutions demonstra um entendimento claro e prático de como a GRC atua na proteção de ativos críticos. Este projeto não é apenas um guia, mas uma prova de que a segurança cibernética deve ser uma função estratégica e contínua, integrada a todos os aspectos de um negócio. A documentação completa serve como base para auditorias futuras e para a construção de uma cultura de segurança robusta.
