# AWS Landing Zone Lab

> Lab público de construção de uma AWS Landing Zone do zero: Control Tower, AFT, governança multi-conta, baseline de segurança, networking e IaC.

> **Status:** 🟡 Em construção · Semana 1 de 12 · Atualizado semanalmente

---

## 🎯 Por que esse lab existe

Arquiteto sênior atuando em ambiente corporativo aprende profundo, mas raramente expõe processo de decisão publicamente. Esse repositório é uma tentativa honesta de mudar isso:

- Documentar **cada decisão arquitetural** via ADRs
- Mostrar **erro, custo e correção** — não só o resultado final
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







## 📩 Contato

- 💼 [LinkedIn](https://www.linkedin.com/in/diego-nery-2a06151a7/)
- 📝 [Medium](https://medium.com/@diegonery465)
- 🌐 [raidsolutions.com.br](https://www.raidsolutions.com.br)
- ✉️ contato@raidsolutions.com.br
