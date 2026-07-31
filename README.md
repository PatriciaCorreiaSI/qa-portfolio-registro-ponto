# QA — Sistema de Registro de Ponto (projeto de estudo)

Portfólio de **QA / Teste de Software** demonstrando desenho de casos de teste, rastreabilidade requisito → caso → defeito e reporte de bugs no padrão profissional.

> ⚠️ **Aviso:** este é um **sistema fictício**, criado para fins de estudo. Nomes de usuário, senhas, clientes, evidências e cenários são **ilustrativos e não reais**, e não representam nenhum produto ou empresa.

---

## Sobre o projeto

Este repositório documenta o trabalho de QA sobre um sistema web fictício de **registro de ponto e gestão de horas por projeto**. O objetivo é mostrar, na prática, como eu:

- escrevo casos de teste formais **a partir dos requisitos, antes de executar** (teste por cobertura, não por sorte);
- mantenho uma **matriz de rastreabilidade** ligando cada funcionalidade aos casos que a cobrem;
- reporto defeitos de forma reproduzível, separando **severidade** (impacto técnico) de **prioridade** (urgência de negócio).

## Sistema sob teste (fictício)

Aplicação web com dois perfis de acesso:

- **Funcionário** — faz login, cria/edita/exclui projetos e lança horas trabalhadas. Só enxerga e gerencia os próprios dados.
- **Admin** — aprova e fecha o mês, reabre o mês, exporta o PDF da folha e gerencia (cria/edita/exclui) as horas lançadas pelos funcionários.

As regras de negócio testadas incluem controle de permissões (o que cada perfil pode ou não fazer), bloqueio de exclusão de projeto com horas lançadas, fechamento/reabertura de mês e isolamento de dados entre funcionários.

## Estratégia de teste

- **Casos escritos antes da execução**, a partir dos critérios de aceite.
- Cobertura de **cenários positivos e negativos** (ex.: login válido × senha incorreta; excluir projeto próprio × de outro usuário; com × sem horas lançadas).
- Ênfase em **testes de autorização/controle de acesso** entre perfis.
- Cada caso com ID único, pré-condições, passos numerados, dados de teste e resultado esperado × obtido.
- Defeitos rastreados de volta ao caso que os revelou.

## Conceitos ISTQB aplicados

- **Erro / Defeito / Falha** — a falha observada na execução é registrada como resultado obtido; o defeito correspondente vira um bug report.
- **Severidade × Prioridade** — colunas separadas em cada caso e bug (ex.: BUG-002 tem severidade Alta, mas prioridade Baixa por ser fluxo pouco frequente).
- **Ciclo de vida do defeito** — Novo → Atribuído → Em correção → Retorno para teste → Fechado / Reaberto.
- **Rastreabilidade** — matriz ligando requisito, caso de teste e defeito.
- **Níveis e tipos de teste** — foco em teste funcional e de autorização em nível de sistema, via interface.

## Resultados (execução atual)

16 casos de teste desenhados; 3 defeitos identificados e reportados.

| Status | Casos |
|---|---|
| ✅ Passou | 8 |
| ❌ Falhou | 3 |
| ⚪ Não executado | 4 |
| 🔵 Em execução | 1 |
| **Total** | **16** |

Defeitos abertos: **BUG-002** (CT-005), **BUG-003** (CT-008), **BUG-004** (CT-014).

## Documentação

- 📋 [Casos de Teste](docs/casos-de-teste.md) — os 16 casos completos.
- 🐞 [Relatórios de Bug](docs/relatorios-de-bug.md) — defeitos reproduzíveis, um por bloco.
- 📑 [Lista Consolidada de Bugs](docs/lista-de-bugs.md) — visão geral dos defeitos em tabela.
- 🔗 [Matriz de Rastreabilidade](docs/matriz-rastreabilidade.md) — requisito → caso → status → defeito.
- 📖 [Guia de Boas Práticas](docs/guia-de-uso.md) — referência de bolso para os templates.
- 📊 [Planilha original](qa-projeto-registro-ponto-v1.xlsx) — todos os templates em `.xlsx`.

## Estrutura do repositório

```
.
├── README.md
├── qa-projeto-registro-ponto-v1.xlsx
└── docs/
    ├── casos-de-teste.md
    ├── relatorios-de-bug.md
    ├── lista-de-bugs.md
    ├── matriz-rastreabilidade.md
    └── guia-de-uso.md
```

## Próximos passos (em progresso)

Este é o pilar de **teste manual e desenho de casos** do meu portfólio. As próximas fases adicionam automação:

- **Automação E2E** dos casos com **Playwright** (Page Object Model, seletores estáveis, asserções).
- **Testes de API** com **Postman**.
- **CI/CD** com **GitHub Actions** rodando a suíte a cada push.

---

*Portfólio de estudo em QA. Feedback é bem-vindo.*
