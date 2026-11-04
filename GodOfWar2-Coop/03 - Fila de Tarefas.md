# Fila de Tarefas — GodOfWar2-Coop

## Como utilizar

Cada tarefa deve ter um identificador único.

Uma tarefa só pode ser executada depois de receber autorização quando envolver instalação, compilação, alteração de arquivos, interação com o PCSX2 ou acesso à memória do jogo.

Não iniciar tarefas apenas porque foram sugeridas por uma IA.

## Tarefas pendentes

### TASK-001 — Diagnosticar falha na compilação de binutils

- **Status:** Em investigação
    
- **Responsável:** Cline
    
- **Objetivo:** Identificar a causa do erro `cd: null directory` durante a criação das bibliotecas libctf.
    
- **Prioridade:** Alta
    
- **Restrições:** Não apagar arquivos, limpar diretórios de build ou repetir comandos `make -n` que possam executar receitas.
    
- **Próximo resultado esperado:** Diagnóstico sustentado por evidências e proposta de correção.
    
- **Autorização:** Investigar apenas. Nova compilação exige autorização específica.
    

### TASK-002 — Investigar transformação 3D de Kratos

- **Status:** Pendente
    
- **Responsável:** Cline
    
- **Objetivo:** Localizar a transformação aplicada ao modelo antes do envio dos vértices ao GS.
    
- **Prioridade:** Alta
    
- **Ponto de partida:** Grupos GS #065–#069 e análise do pipeline VU1.
    
- **Próximo resultado esperado:** Identificação de funções, dados ou instruções relacionadas à transformação do modelo.
    

### TASK-003 — Avaliar viabilidade de duplicação do modelo

- **Status:** Pendente
    
- **Responsável:** ChatGPT, com revisão do Gemini
    
- **Objetivo:** Avaliar se a transformação identificada permite renderizar um segundo Kratos com posição e orientação independentes.
    
- **Dependência:** Resultados da TASK-002.
    
- **Próximo resultado esperado:** Proposta técnica com limitações e testes necessários.
    

### TASK-004 — Investigar câmera independente

- **Status:** Pendente
    
- **Responsável:** Cline
    
- **Objetivo:** Identificar como a câmera é configurada e se é possível manter duas perspectivas independentes.
    
- **Dependência:** Avanço na análise da renderização 3D.
    
- **Próximo resultado esperado:** Identificação dos dados e funções envolvidos na câmera.
    

## Modelo para novas tarefas

### TASK-XXX — Título

- **Status:** Pendente / Em investigação / Aguardando autorização / Bloqueada / Concluída / Cancelada.
    
- **Responsável:**
    
- **Objetivo:**
    
- **Prioridade:**
    
- **Dependências:**
    
- **Restrições:**
    
- **Autorização necessária:**
    
- **Resultado esperado:**
    

## Histórico

Registrar mudanças de responsável, prioridade, status, escopo ou autorização.

Nenhuma tarefa deve ser considerada concluída sem relatório e evidências.