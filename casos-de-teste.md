# Casos de Teste

> Sistema fictício de registro de ponto. Dados de teste ilustrativos (não reais).

### CT-001 — Login com credenciais válidas
**Módulo:** Login · **Severidade:** Crítica · **Prioridade:** Alta · **Status:** ⚪ Não executado

| Campo | Detalhe |
|---|---|
| Pré-condições | Usuário cadastrado e ativo |
| Passos | 1. Abrir a tela de login<br>2. Informar e-mail e senha válidos<br>3. Clicar em Entrar |
| Dados de teste | e-mail: ana@x.com / senha: Abc123! |
| Resultado esperado | Usuário autenticado e redirecionado ao dashboard |
| Resultado obtido | — |

### CT-002 — Login com senha incorreta
**Módulo:** Login · **Severidade:** Alta · **Prioridade:** Alta · **Status:** ⚪ Não executado

| Campo | Detalhe |
|---|---|
| Pré-condições | Usuário cadastrado |
| Passos | 1. Abrir a tela de login<br>2. Informar e-mail válido e senha errada<br>3. Clicar em Entrar |
| Dados de teste | e-mail: ana@x.com / senha: errada |
| Resultado esperado | Mensagem 'Credenciais inválidas' e permanência na tela de login |
| Resultado obtido | — |

### CT-003 — Campo e-mail obrigatório
**Módulo:** Cadastro · **Severidade:** Média · **Prioridade:** Média · **Status:** ⚪ Não executado

| Campo | Detalhe |
|---|---|
| Pré-condições | Estar na tela de cadastro |
| Passos | 1. Deixar o campo e-mail vazio<br>2. Preencher os demais campos<br>3. Clicar em Cadastrar |
| Dados de teste | e-mail: (vazio) |
| Resultado esperado | Sistema bloqueia e exibe 'E-mail é obrigatório' |
| Resultado obtido | — |

### CT-004 — Criar projeto com dados válidos
**Módulo:** Funcionário · **Severidade:** Alta · **Prioridade:** Alta · **Status:** ✅ Passou

| Campo | Detalhe |
|---|---|
| Pré-condições | 1. Estar logado como Funcionário<br>2. Ter botão +Novo Projeto habilitado |
| Passos | 1. Logar com suas credenciais de funcionário<br>2. Clicar no menu em Registrar Pontos<br>3. Clicar no botão +Novo Projeto<br>4. Preencher campos do modal Novo Projeto<br>5. Clicar em criar projeto |
| Dados de teste | user: ana@x.com/<br>senha:Abc123!<br>nome do Projeto: Teste 1<br>cliente: Cliente Exemplo<br>Alocar funcionário: ana |
| Resultado esperado | Novo projeto é criado com sucesso e aparece associado ao seu cliente e funcionários alocados na aba Projetos do login do admin.<br>Novo projeto fica disponível na droplist que preenche o campo "Projeto" no Registro de Ponto do funcionário alocado a este projeto. |
| Resultado obtido | Novo projeto é criado com sucesso e aparece associado ao seu cliente e funcionários alocados na aba Projetos do login do admin.<br>Novo projeto fica disponível na droplist que preenche o campo "Projeto" no Registro de Ponto do funcionário alocado a este projeto. |

### CT-005 — Editar projeto criado pelo próprio funcionário
**Módulo:** Funcionário · **Severidade:** Alta · **Prioridade:** Baixa · **Status:** ❌ Falhou

| Campo | Detalhe |
|---|---|
| Pré-condições | 1. Estar logado como Funcionário<br>2. Ter  cadastrado pelo menos 1 projeto no sistema |
| Passos | 1. Logar com suas credenciais de funcionário<br>2. Clicar no menu em Registrar Pontos<br>3. Abrir droplist no campo "Projeto"<br>4. Clicar no lápis ao lado direito do nome do Projeto que deseja editar<br>5. Salvar alteração |
| Dados de teste | user: ana@x.com/<br>senha:Abc123!<br>nome do Projeto: Teste 1 |
| Resultado esperado | Usuario funcionário com botao +Novo projeto habilitado consegue abrir droplist no campo "Projeto" na aba "Registrar Ponto" e visualizar lápis de edição ao lado direito<br>Usuario consegue abrir modal de edição, alterar campos e salvar alterações |
| Resultado obtido | Usuario não visualiza lápis de edição.<br>Usuário não consegue editar e salvar alterações em projeto criado por ele |

### CT-006 — Excluir Projeto criado pelo usuário sem horas lançadas
**Módulo:** Funcionário · **Severidade:** Alta · **Prioridade:** Alta · **Status:** ✅ Passou

| Campo | Detalhe |
|---|---|
| Pré-condições | Funcionário ter permissão para criar/editar/excluir projeto |
| Passos | 1. Logar com suas credenciais de funcionário<br>2. Clicar no campo Projetos e abrir droplist com nome dos projetos<br>3. Identificar Projeto criado pelo usuário<br>4. Ver lápis de edição renderizado e clicar<br>5. Abrir modal de edição<br>6. Clicar em excluir<br>7. Confirmar exclusão |
| Dados de teste | "user: ana@x.com/<br>senha:Abc123!<br>nome do Projeto: Teste 1" |
| Resultado esperado | Usuário consegue excluir projeto criado por ele sem horas lançadas no projeto. |
| Resultado obtido | Usuário consegue excluir projeto criado por ele sem horas lançadas no projeto. |

### CT-007 — Excluir Projeto não criado pelo usuário sem horas lançadas
**Módulo:** Funcionário · **Severidade:** Alta · **Prioridade:** Média · **Status:** ✅ Passou

| Campo | Detalhe |
|---|---|
| Pré-condições | Existir projeto criado por outro usuário |
| Passos | 1. Logar com suas credenciais de funcionário<br>2. Clicar no campo Projetos e abrir droplist com nome dos projetos |
| Dados de teste | "user: bruno@x.com/<br>senha:Def123!<br>nome do Projeto: Teste 1" |
| Resultado esperado | Usuário não consegue visualizar lápis de edição e não exclui nenhum projeto. |
| Resultado obtido | Usuário não consegue visualizar lápis de edição nem excluir nenhum projeto. |

### CT-008 — Excluir Projeto criado pelo usuário com horas lançadas
**Módulo:** Funcionário · **Severidade:** Média · **Prioridade:** Média · **Status:** ❌ Falhou

| Campo | Detalhe |
|---|---|
| Pré-condições | 1. Funcionário ter permissão para criar/editar/excluir projeto<br>2. Projeto conter horas lançadas |
| Passos | 1. Logar com suas credenciais de funcionário<br>2. Clicar no campo Projetos e abrir droplist com nome dos projetos<br>3. Identificar Projeto criado pelo usuário<br>4. Ver lápis de edição renderizado e clicar<br>5. Abrir modal de edição<br>6. Clicar em excluir<br>7. Confirmar exclusão<br>8. Visualizar mensagem de erro do sistema que impede a exclusão |
| Dados de teste | "user: ana@x.com/<br>senha:Abc123!<br>nome do Projeto: Teste 1" |
| Resultado esperado | Usuário não consegue excluir projeto criado por ele com horas lançadas no projeto.<br>Sistema mostra mensagem de erro e impede a exclusão. |
| Resultado obtido | Usuário não consegue excluir projeto criado por ele com horas lançadas no projeto.<br>Sistema não mostra mensagem de erro. Sistema impede a exclusão. |

### CT-009 — Excluir Projeto não criado pelo usuário com horas lançadas
**Módulo:** Funcionário · **Severidade:** Média · **Prioridade:** Baixa · **Status:** ✅ Passou

| Campo | Detalhe |
|---|---|
| Pré-condições | 1. Existir projeto criado por outro usuário<br>2. Projeto conter horas lançadas |
| Passos | 1. Logar com suas credenciais de funcionário<br>2. Clicar no campo Projetos e abrir droplist com nome dos projetos |
| Dados de teste | "user: bruno@x.com/<br>senha:Def123!<br>nome do Projeto: Teste 1" |
| Resultado esperado | Usuário não consegue visualizar lápis de edição e não exclui nenhum projeto. |
| Resultado obtido | Usuário não consegue visualizar lápis de edição nem excluir nenhum projeto. |

### CT-010 — Aprova horas trabalhadas do mês
**Módulo:** Admin · **Severidade:** Alta · **Prioridade:** Alta · **Status:** ✅ Passou

| Campo | Detalhe |
|---|---|
| Pré-condições | 1. Estar logado como Admin<br>2. Visualizar Dashboard das horas trabalhadas<br>3. Fechar lançamento do mês |
| Passos | 1. Logar com suas credenciais de admin<br>2. Clicar na Página Horas da Folha<br>3. Clicar no botão "Fechar lançamento do mês"<br>4. Visualizar mensagem de sucesso |
| Dados de teste | "user: admin<br>senha: admin1234" |
| Resultado esperado | Ver botão do Fechar mês se converter para Mês Fechado.<br>Visualizar mensagem na tela "Mês fechado com sucesso" |
| Resultado obtido | User admin consegue fechar mês ao clicar no botão Fechar mês. <br>User admin visualiza mensagem de sucesso ao fechar mês |

### CT-011 — Baixar PDF de mês fechado
**Módulo:** Admin · **Severidade:** Alta · **Prioridade:** Média · **Status:** ⚪ Não executado

| Campo | Detalhe |
|---|---|
| Pré-condições | 1. Ter ao menos 1 mês fechado no sistema |
| Passos | 1. Logar com suas credenciais de admin<br>2. Clicar na Página Horas da Folha<br>3. Visualizar mês fechado<br>4. Clicar no botão Exportar PDF<br>5. Abrir arquivo PDF baixado |
| Dados de teste | "user: admin<br>senha: admin1234" |
| Resultado esperado | Visualizar PDF disponível para download<br>Abrir arquivo PDF |
| Resultado obtido | — |

### CT-012 — Reabrir mês fechado
**Módulo:** Admin · **Severidade:** Alta · **Prioridade:** Baixa · **Status:** 🔵 Em execução

| Campo | Detalhe |
|---|---|
| Pré-condições | 1. Ter ao menos 1 mês fechado no sistema |
| Passos | 1. Logar com suas credenciais de admin<br>2. Clicar na Página Horas da Folha<br>3. Visualizar mês fechado<br>4. Clicar no botão Reabrir mês [mes][ano] |
| Dados de teste | "user: admin<br>senha: admin1234"<br>Mes fechado: junho 2026 |
| Resultado esperado | User admin visualiza mês reaberto.<br>User admin visualiza botão Fechar mês disponível |
| Resultado obtido | User admin visualiza mês reaberto.<br>User admin visualiza botão Fechar mês disponível |

### CT-013 — Editar hora lançada de funcionário
**Módulo:** Admin · **Severidade:** Alta · **Prioridade:** Alta · **Status:** ✅ Passou

| Campo | Detalhe |
|---|---|
| Pré-condições | 1. Ter ao menos 1 hora de funcionário lançada no sistema |
| Passos | 1. Logar com suas credenciais de admin<br>2. Clicar na Página Ponto de Funcionários<br>3. Filtrar pelo nome do funcionário<br>4. Clicar no lápis de edição<br>5. Editar modal de edição<br>6. Salvar alterações |
| Dados de teste | "user: admin<br>senha: admin1234"<br>Funcionário: José Silva |
| Resultado esperado | User admin consegue editar horas lançadas pelo funcionário.<br>User admin consegue salvar alterações feitas |
| Resultado obtido | User admin consegue editar horas lançadas pelo funcionário.<br>User admin consegue salvar alterações feitas |

### CT-014 — Excluir hora lançada de funcionário
**Módulo:** Admin · **Severidade:** Média · **Prioridade:** Baixa · **Status:** ❌ Falhou

| Campo | Detalhe |
|---|---|
| Pré-condições | 1. Ter ao menos 1 hora de funcionário lançada no sistema |
| Passos | 1. Logar com suas credenciais de admin<br>2. Clicar na Página Ponto de Funcionários<br>3. Filtrar pelo nome do funcionário<br>4. Clicar no X no registro que se deseja excluir |
| Dados de teste | "user: admin<br>senha: admin1234"<br>Funcionário: José Silva<br>Data do ponto: 01-06-2026 |
| Resultado esperado | User admin consegue excluir registro de hora lançada pelo funcionário.<br>User admin visualiza mensagem de "Registro de hora excluído com sucesso" |
| Resultado obtido | User admin consegue excluir registro de hora lançada pelo funcionário.<br>User não visualiza mensagem de "Registro de hora excluído com sucesso" |

### CT-015 — Criar hora lançada de funcionário
**Módulo:** Admin · **Severidade:** Alta · **Prioridade:** Alta · **Status:** ✅ Passou

| Campo | Detalhe |
|---|---|
| Pré-condições | 1. Ter ao menos 1 funcionário registrado no sistema |
| Passos | 1. Logar com suas credenciais de admin<br>2. Clicar na Página Ponto de Funcionários<br>3. Filtrar pelo nome do funcionário<br>4. Clicar no botão "Lançar Hora"<br>5. Editar modal de lançar hora<br>6. Salvar registro |
| Dados de teste | "user: admin<br>senha: admin1234"<br>Funcionário: José Silva |
| Resultado esperado | User admin consegue criar novo registro de hora para funcionário cadastrado no sistema.<br>Novo registro de hora fica visível na  Página Horas da Folha vinculada ao funcionário. |
| Resultado obtido | User admin consegue criar novo registro de hora para funcionário cadastrado no sistema.<br>Novo registro de hora fica visível na  Página Horas da Folha vinculada ao funcionário. |

### CT-016 — User Funcionário não consegue visualizar horas de outro funcionário
**Módulo:** Autorização/controle de acesso via interface · **Severidade:** Alta · **Prioridade:** Alta · **Status:** ✅ Passou

| Campo | Detalhe |
|---|---|
| Pré-condições | 1. Ter ao menos 2 funcionários registrados no sistema |
| Passos | 1. Logar com suas credenciais de funcionário<br>2. Clicar no menu em Histórico de Pontos |
| Dados de teste | "user: bruno@x.com/<br>senha:Def123! |
| Resultado esperado | User funcionário logado visualiza apenas as horas lançadas vinculadas ao seu user. |
| Resultado obtido | User funcionário logado visualiza apenas as horas lançadas vinculadas ao seu user. |
