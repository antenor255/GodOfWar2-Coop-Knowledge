# Registro de Decisões Técnicas

Este documento registra decisões que afetam a arquitetura, os métodos de investigação e a implementação do projeto.

Uma decisão não deve ser alterada silenciosamente. Qualquer revisão precisa apresentar justificativa técnica e evidências.

## Decisões

### DEC-001 — Priorizar a duplicação da renderização 3D

**Status:** Em investigação.

**Decisão:** Priorizar a investigação da duplicação do modelo 3D de Kratos com transformação independente, mantendo uma única lógica de jogo.

**Motivo:** Duplicar apenas comandos GS pode produzir uma cópia visual 2D, sem garantir um segundo personagem 3D independente.

**Condição para revisão:** Evidência de que outra abordagem oferece uma solução mais adequada.

### DEC-002 — Tratar GS #065–#069 como candidatos à renderização de Kratos

**Status:** Aceita como hipótese operacional.

**Decisão:** Utilizar esses grupos como ponto de partida para investigar a renderização do personagem.

**Evidência:** Captura GS na qual Kratos estava inteiro e claramente visível. O usuário confirmou a identificação visual.

**Limitação:** Ainda não foi demonstrado como esses grupos se relacionam com a transformação 3D anterior ao GS.

### DEC-003 — Não considerar `0x003355C0` uma estrutura completa do jogador

**Status:** Pendente de confirmação.

**Decisão:** Tratar o endereço como região candidata a coordenadas, não como estrutura completa de Kratos.

**Evidência:** Dois componentes float mudaram entre snapshots de parado e movimento.

**Condição para revisão:** Identificação dos campos e comprovação da relação com o jogador por testes ou análise de código.

### DEC-004 — Gemini como revisor independente

**Status:** Aceita.

**Decisão:** Utilizar Gemini Free para revisar propostas e conclusões técnicas importantes.

**Limitação:** O Gemini recebe apenas os materiais enviados. Não possui acesso direto ao projeto ou ao ambiente local.

### DEC-005 — Codex sob demanda

**Status:** Aceita.

**Decisão:** Utilizar Codex apenas quando houver necessidade de revisão independente de código, investigação de erros complexos ou comparação de implementações.

### DEC-006 — Cline como agente principal de execução

**Status:** Aceita.

**Decisão:** Cline será responsável pelas investigações e execuções autorizadas no workspace.

**Limitação:** Cada instalação, compilação, alteração de arquivo ou interação sensível continua dependendo de autorização específica do usuário.

## Modelo para novas decisões

### DEC-XXX — Título

- **Status:** Proposta / Em investigação / Aceita / Rejeitada / Substituída.
    
- **Data:**
    
- **Decisão:**
    
- **Motivo:**
    
- **Evidências:**
    
- **Limitações:**
    
- **Condição para revisão:**
    

## Histórico de alterações

Registrar aqui qualquer mudança de decisão, indicando a decisão anterior, a nova decisão, a justificativa e as evidências que motivaram a alteração.