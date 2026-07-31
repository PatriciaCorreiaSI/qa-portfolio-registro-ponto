# Matriz de Rastreabilidade

Liga cada requisito/funcionalidade aos casos de teste que o cobrem e ao status atual.

| Funcionalidade / Regra | Casos de teste | Status | Observações |
|---|---|---|---|
| Login | CT-001, CT-002 | ⚪ Não executado |  |
| Cadastro | CT-003 | ⚪ Não executado |  |
| Criar Projeto | CT-004 | ✅ Passou |  |
| Editar Projeto criado | CT-005 | ❌ Falhou | BUG-002 |
| Excluir Projeto criado pelo próprio usuário | CT-006 | ✅ Passou |  |
| Excluir Projeto criado por outro usuário | CT-007 | ✅ Passou |  |
| Excluir Projeto criado pelo próprio usuário com horas lançadas | CT-008 | ❌ Falhou | BUG-003. Retestar após correção do BUG. |
| Excluir Projeto criado por outro usuário com horas lançadas | CT-009 | ✅ Passou |  |
| Aprova horas trabalhadas do mês | CT-010 | ✅ Passou |  |
| Baixar PDF de mês fechado | CT-011 | ⚪ Não executado |  |
| Reabrir mês fechado | CT-012 | 🔵 Em execução | Executar em staging para não poluir produção |
| Admin editar horas de funcionário | CT-013 | ✅ Passou |  |
| Admin exclui horas de funcionário | CT-014 | ❌ Falhou | BUG-004 |
| Admin criar horas de funcionário | CT-015 | ✅ Passou |  |
| Autorização/controle de acesso via interface | CT-016 | ✅ Passou | Automatizar teste de regressão com Playwright |