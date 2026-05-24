# AWS Landing Zone Lab

> Lab público de construção de uma AWS Landing Zone do zero: Control Tower, AFT, governança multi-conta, baseline de segurança, networking e IaC.

> **Status:** 🟡 Em construção · Semana 1 de 12 · Atualizado semanalmente

---

## 🎯 Por que esse lab existe

Arquiteto atuando em ambiente corporativo aprende profundo, mas raramente expõe processo de decisão publicamente. Esse repositório é uma tentativa honesta de mudar isso:

- Documentar **cada decisão arquitetural** via ADRs
- Mostrar **erro, custo e correção**, não só o resultado final
- Construir Landing Zone do zero, sem atalhos, sem material de cliente
- Servir como referência pra quem quer entender Landing Zone na prática

Sou Diego Nery, Cloud Platform Architect. <!---Mais sobre meu trabalho em [raidsolutions.com.br](https://www.raidsolutions.com.br).-->

---

## 🗓️ Roadmap das 12 semanas

| Semana | Entregável | Status |
|---|---|---|
| 1 | Setup inicial: conta isolada, MFA root, IAM Identity Center, billing alarms, repo público | ✅ Concluído |
| 2 | AWS Organizations + estrutura inicial de OUs | ⬜ |
| 3 | Control Tower habilitado + primeiras 2 contas filhas | ⬜ |
| 4 | AFT (Account Factory for Terraform) configurado | ⬜ |
| 5 | SCPs aplicadas (deny region, deny root, deny disable CloudTrail) | ⬜ |
| 6 | CloudTrail org-wide + AWS Config | ⬜ |
| 7 | GuardDuty + Security Hub | ⬜ |
| 8 | VPC base + Transit Gateway entre contas | ⬜ |
| 9 | IPAM com pool definido | ⬜ |
| 10 | Pipeline Terraform via GitHub Actions | ⬜ |
| 11 | Documentação completa: README, ADRs, diagramas | ⬜ |
| 12 | Artigo Medium consolidando a jornada + tour final | ⬜ |

**Legenda:** ⬜ Não iniciado · 🟡 Em andamento · ✅ Concluído

---

## 🏗️ Arquitetura-alvo (versão final)

> Diagrama em construção. Será adicionado nas semanas 8-11.

A Landing Zone final terá:

- **AWS Organizations** com OUs estruturadas (Workloads, Sandbox, Security, Infrastructure)
- **Control Tower + AFT** para account vending automatizado
- **SCPs (Service Control Policies)** aplicadas por OU
- **Baseline de segurança** centralizada: CloudTrail, AWS Config, GuardDuty, Security Hub
- **Networking** com Transit Gateway e IPAM
- **IAM Identity Center** como provedor SSO
- **Pipeline Terraform** com GitHub Actions

---

## 📐 Decisões Arquiteturais (ADRs)

ADRs são adicionadas na pasta [`/docs/adr`](./docs/adr) à medida que decisões são tomadas.

> ADRs publicadas aparecerão aqui ao longo das 12 semanas.

---

## 💰 Controle de custo

O lab é mantido com disciplina rigorosa de **tear down**. Componentes caros (Transit Gateway, NAT Gateway) sobem só durante sessões de trabalho e são destruídos ao final.

**Alvo de custo:** USD 30-60 / mês
**Orçamento máximo do ciclo (12 semanas):** USD 110 (~R$ 600)

Custos detalhados serão publicados semanalmente em [`/docs/cost-log.md`](./docs/cost-log.md).

---

## 📚 Stack utilizada

- **Cloud:** AWS (única região principal: `sa-east-1`)
- **IaC:** Terraform 1.7+
- **CI/CD:** GitHub Actions, GitLab ou Bitbucket (irei escolher e atualizar depois)
- **Documentação:** Markdown + Mermaid (para diagramas)

---

## 📖 Posts publicados sobre o lab

Cada semana gera 1 post no LinkedIn documentando o componente entregue e as decisões técnicas envolvidas.

> Links serão adicionados aqui à medida que os posts forem publicados.

| Semana | Post | Link |
|---|---|---|
| 1 | Por que arquiteto sênior precisa de portfólio público | em breve |

---

## ⚠️ Sobre uso do código

Esse é um **lab de aprendizado público**. Código aqui:

- ✅ Pode ser estudado, referenciado e adaptado livremente (licença MIT — ver [LICENSE](./LICENSE))
- ❌ **Não está pronto para produção sem revisão crítica do contexto** específico do seu ambiente
- ❌ Não substitui consultoria especializada para casos reais

Se você precisa de Landing Zone em ambiente real, considere consultoria profissional. Eu atendo via [Raid Solutions](https://www.raidsolutions.com.br).

---

## 📩 Contato

- 💼 [LinkedIn](https://www.linkedin.com/in/diego-nery-2a06151a7/)
- 📝 [Medium](https://medium.com/@diegonery465)
- 🌐 [raidsolutions.com.br](https://www.raidsolutions.com.br)
- ✉️ contato@raidsolutions.com.br
