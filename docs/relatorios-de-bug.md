# Relatórios de Bug (Defeitos)

> Reportados durante a execução dos casos de teste. Sistema e evidências fictícios.

## BUG-002 — Ícone de edição (lápis) não é renderizado ao lado de projeto criado pelo próprio funcionário (aba Registrar Ponto)

| Campo | Detalhe |
|---|---|
| Título | Ícone de edição (lápis) não é renderizado ao lado de projeto criado pelo próprio funcionário (aba Registrar Ponto) |
| Módulo / Funcionalidade | Funcionário |
| Ambiente | App v1.0.0 \| Chrome 126 \| Windows 11 \| Desktop |
| Pré-condições | 1. Estar logado como Funcionário<br>2. Ter  cadastrado pelo menos 1 projeto no sistema |
| Passos para Reproduzir | 1. Logar com suas credenciais de funcionário<br>2. Clicar no menu em Registrar Pontos<br>3. Abrir droplist no campo "Projeto"<br>4. Clicar no lápis ao lado direito do nome do Projeto criado pelo funcionário |
| Resultado Esperado | Renderiza o lápis clicável ao lado direito do nome do Projeto criado pelo funcionário.<br>Usuario consegue abrir modal de edição, alterar campos e salvar alterações. |
| Resultado Obtido | Não renderiza o lápis clicável ao lado direito do nome do Projeto criado pelo funcionário.<br>Usuario não consegue abrir modal de edição, alterar campos e salvar alterações. |
| Severidade | Alta |
| Prioridade | Baixa (fluxo pouco frequente) |
| Reprodutibilidade | Sempre |
| Status | Em correção |
| Reportado por | QA testador |
| Data | 08/07/2026 |
| Observações | Edição só é possível pelo login admin |

## BUG-003 — Sistema não mostra mensagem de erro ao impedir exclusão de projeto com horas lançadas.

| Campo | Detalhe |
|---|---|
| Título | Sistema não mostra mensagem de erro ao impedir exclusão de projeto com horas lançadas. |
| Módulo / Funcionalidade | Funcionário |
| Ambiente | App v1.0.0 \| Chrome 126 \| Windows 11 \| Desktop |
| Pré-condições | 1. Funcionário ter permissão para criar/editar/excluir projeto<br>2. Projeto conter horas lançadas |
| Passos para Reproduzir | 1. Logar com suas credenciais de funcionário<br>2. Clicar no campo Projetos e abrir droplist com nome dos projetos<br>3. Identificar Projeto criado pelo usuário<br>4. Ver lápis de edição renderizado e clicar<br>5. Abrir modal de edição<br>6. Clicar em excluir<br>7. Confirmar exclusão |
| Resultado Esperado | Usuário não consegue excluir projeto criado por ele com horas lançadas no projeto.<br>Sistema mostra mensagem de erro e impede a exclusão. |
| Resultado Obtido | Usuário não consegue excluir projeto criado por ele com horas lançadas no projeto.<br>Sistema não mostra mensagem de erro. Sistema impede a exclusão. |
| Severidade | Média |
| Prioridade | Média |
| Reprodutibilidade | Sempre |
| Status | Atribuído |
| Reportado por | QA testador |
| Data | 27/07/2026 |
| Observações | Projeto precisa ter horas lançadas |

## BUG-004 — Sistema não mostra mensagem "Registro de hora excluído com sucesso" ao user admin  ao excluir lançamento de hora de funcionário

| Campo | Detalhe |
|---|---|
| Título | Sistema não mostra mensagem "Registro de hora excluído com sucesso" ao user admin  ao excluir lançamento de hora de funcionário |
| Módulo / Funcionalidade | Admin |
| Ambiente | App v1.0.0\| Chrome 126 \| Windows 11 \| Desktop |
| Pré-condições | 1. Ter ao menos 1 hora de funcionário lançada no sistema |
| Passos para Reproduzir | 1. Logar com suas credenciais de admin<br>2. Clicar na Página Ponto de Funcionários<br>3. Filtrar pelo nome do funcionário<br>4. Clicar no X no registro que se deseja excluir |
| Resultado Esperado | User admin consegue excluir registro de hora lançada pelo funcionário.<br>User admin visualiza mensagem de "Registro de hora excluído com sucesso" |
| Resultado Obtido | User admin consegue excluir registro de hora lançada pelo funcionário.<br>User não visualiza mensagem de "Registro de hora excluído com sucesso" |
| Severidade | Média |
| Prioridade | Baixa |
| Reprodutibilidade | Sempre |
| Status | Novo |
| Reportado por | QA testador |
| Data | 31/07/2026 |
| Observações | Funcionário precisa ter horas lançadas |
