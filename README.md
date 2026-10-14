# COMP0513 – Representação de Conhecimento e Raciocínio Automático

## Parte I – Unidade 01 (Aulas 01–10) – Grupo 7

Mini-sistema especialista em **Lógica de Primeira Ordem (LPO)** para o domínio de uma **Biblioteca Universitária** (controle de acervo e empréstimos), implementado em **Python** com a biblioteca **aima3** (aima-python).

O sistema infere automaticamente o **atraso de devolução** e o **bloqueio para novos empréstimos** a partir de fatos e regras gerais — conclusões que **não** estão armazenadas explicitamente. Além do motor lógico (encadeamento para frente e para trás, unificação/MGU, resolução), inclui uma camada de **sistema de produção** com memória de trabalho, conjunto de conflito e ações ADD/REMOVE/MODIFY, e demonstração de **atualização dinâmica** (`retract`).

**Abrir no Colab:** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Tyxiel/rc-ra/blob/main/COMP0513_ParteI_Grupo7_Colab.ipynb)

---

### Integrantes

| Nome | RA |
|---|---|
| SAMUEL CAMPOS DOS SANTOS | 202600081368 |
| CAIO VICTOR PRADO CRUZ | 202100011234 |
| JOAO PEDRO CHAVES OLIVEIRA | 202600046064 |

---

### Estrutura do repositório

| Arquivo | Descrição |
|---|---|
| `COMP0513_ParteI_Grupo7_Colab.ipynb` | Notebook principal (já executado, com saídas) — abre direto no Google Colab |
| `README.md` | Este arquivo |

### Como executar

**No Google Colab (recomendado):** clique no selo *Open in Colab* acima (funciona quando o repositório é público e o link direto está preenchido) ou faça `Arquivo → Fazer upload de notebook` e execute tudo com `Ambiente de execução → Executar tudo`. A primeira célula instala a única dependência (`aima3`).

**Localmente:** requer Python ≥ 3.9 (validado em 3.14) e:

```bash
pip install aima3
jupyter notebook COMP0513_ParteI_Grupo7_Colab.ipynb
```

---

### Link direto do Colab

Repositório (público): **github.com/Tyxiel/rc-ra**

**Abrir o notebook direto no Colab:** https://colab.research.google.com/github/Tyxiel/rc-ra/blob/main/COMP0513_ParteI_Grupo7_Colab.ipynb

O formato `colab.research.google.com/github/<usuario>/<repo>/blob/<branch>/<arquivo>.ipynb` abre qualquer notebook `.ipynb` do GitHub direto no Colab — o repositório precisa ser **público**. *(Alternativa sem GitHub: no Colab, `Arquivo → Salvar uma cópia no Drive`, depois `Compartilhar → Qualquer pessoa com o link` e copie o endereço `.../drive/...`.)*

---

### Conteúdo coberto (checklist Unidade 01)

- Domínio, propósito, escopo e pressupostos explícitos (mundo aberto, temporalidade estática)
- Vocabulário/assinatura com predicados, aridade e ordem dos argumentos
- 13 fatos explícitos (F1–F13) e 5 regras gerais (R1–R5, cláusulas de Horn; R5 existencial teórica)
- 12 perguntas de competência (PC1–PC12), incluindo casos não provados (indeterminação)
- Consultas ground e com variáveis (`ask`, `fol_bc_ask`, `fol_fc_ask`)
- Unificação/MGU (`unify`, `subst`) e exemplo manual de resolução por refutação
- Encadeamento para frente com rastro (regra, substituição θ, novo fato)
- Encadeamento para trás com decomposição de metas
- Sistema de produção: memória de trabalho, 5 regras, ciclo reconhecer–resolver conflito–agir, ADD/REMOVE/MODIFY
- Atualização dinâmica (`retract`/`tell`) e interpretação correta ("deixa de ser derivável" ≠ "falso")
- 7 testes automatizados (7/7 PASS) e limitações declaradas

### Tecnologias

- Python 3 · [aima3](https://pypi.org/project/aima3/) (aima-python): `FolKB`, `expr`, `unify`, `subst`, `fol_fc_ask`, `fol_bc_ask`, `tell`, `ask`, `retract`
- Materiais de referência: AIMA (Russell & Norvig) e Brachman & Levesque, *Knowledge Representation and Reasoning* (2004)
