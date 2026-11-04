# Registro de Evidências — GodOfWar2-Coop

## 1. Objetivo

Centralizar evidências técnicas coletadas durante a investigação.

Toda descoberta importante deve possuir uma fonte identificável e uma interpretação limitada ao que os dados realmente demonstram.

## 2. Classificação das informações

- **FATO — TESTADO:** comportamento observado em teste reproduzível.
    
- **FATO — DOCUMENTADO:** informação confirmada por código, documentação ou especificação técnica.
    
- **HIPÓTESE SUSTENTADA:** interpretação apoiada por evidências, mas ainda não comprovada.
    
- **ESPECULAÇÃO:** possibilidade sem evidência suficiente.
    
- **DESCONHECIDO:** informação ainda não investigada ou inconclusiva.
    

## 3. Modelo de registro

### EVD-XXX — Título da evidência

- **Data:**
    
- **Tarefa relacionada:**
    
- **Classificação:**
    
- **Fonte:** arquivo, endereço, captura, log ou documentação.
    
- **Método de coleta:**
    
- **Condições do teste:**
    
- **Observação direta:**
    
- **Interpretação:**
    
- **O que a evidência demonstra:**
    
- **O que não demonstra:**
    
- **Arquivos associados:**
    
- **Responsável pela coleta:**
    
- **Possibilidade de reprodução:**
    

## 4. Evidências já registradas

### EVD-001 — Alterações em 0x003355C0

- **Classificação:** Hipótese sustentada.
    
- **Fonte:** snapshots binários de estados parado e movimento.
    
- **Observação:** os componentes float em `0x003355C0` e `0x003355C8` mudaram nos pares comparados.
    
- **Interpretação:** região candidata a armazenar coordenadas relacionadas ao jogador.
    
- **Limitação:** não comprova a estrutura completa de Kratos nem identifica definitivamente os eixos.
    

### EVD-002 — Grupos GS candidatos à renderização de Kratos

- **Classificação:** Hipótese operacional.
    
- **Fonte:** capturas GS analisadas e confirmação visual do usuário.
    
- **Observação:** grupos #065–#069 foram associados visualmente ao Kratos inteiro.
    
- **Interpretação:** candidatos úteis para investigar o fluxo de renderização.
    
- **Limitação:** não revelam diretamente a transformação 3D anterior ao GS.
    

### EVD-003 — Região 0x0041D308 sem diferenças

- **Classificação:** Fato — testado.
    
- **Fonte:** comparação entre `KRATOS_CANDIDATE_IDLE_0041D308_512.bin` e `KRATOS_CANDIDATE_MOVE_0041D308_512.bin`.
    
- **Observação:** os 512 bytes comparados eram idênticos.
    
- **Interpretação:** essa região não mudou entre aqueles dois snapshots.
    
- **Limitação:** não prova que a região seja irrelevante para Kratos.
    

## 5. Regras de preservação

- Não sobrescrever evidências antigas.
    
- Preservar os arquivos originais.
    
- Registrar hashes quando disponíveis.
    
- Não alterar a classificação sem justificar a mudança.
    
- Uma hipótese só se torna fato após validação adequada.
    
- Resultados negativos também devem ser registrados.
    
- Divergências entre agentes devem permanecer documentadas.
    

## 6. Histórico de revisões

Registrar alterações de classificação, correções de interpretação e novas validações, sempre indicando a evidência que justificou a mudança.