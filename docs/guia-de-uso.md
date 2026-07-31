# Guia Rápido de Boas Práticas

Referência de bolso para preencher os templates de QA.

### Severidade x Prioridade
Severidade = impacto técnico do defeito. Prioridade = urgência de corrigir para o negócio. Um erro de digitação na home pode ser Severidade Baixa mas Prioridade Alta (é a primeira coisa que o cliente vê).

### Bom título de bug
Específico: diga O QUÊ e ONDE. Ruim: 'Erro no login'. Bom: 'Login trava ao usar e-mail com maiúsculas na tela de acesso'.

### Passos para reproduzir
Numerados, do zero, para que qualquer pessoa reproduza. Comece sempre de um estado conhecido (ex.: 'na tela inicial deslogado').

### Esperado vs. Obtido
Sempre os dois. Sem o esperado, ninguém sabe se é bug ou comportamento correto.

### Ambiente
Versão do app, navegador/SO e dispositivo. Muitos bugs só aparecem em um ambiente.

### Evidência
Print ou vídeo curto. Uma imagem economiza dez linhas de texto e evita mal-entendidos.

### Escreva o caso ANTES
Desenhe o caso de teste a partir do requisito antes de testar. Assim você testa por cobertura, não por sorte.

### Ciclo de vida do bug
Novo → Atribuído → Em correção → Retorno para teste → Fechado (ou Reaberto se voltar a falhar).
