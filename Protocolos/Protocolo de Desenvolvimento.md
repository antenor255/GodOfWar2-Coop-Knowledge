# Protocolo de Desenvolvimento — GodOfWar2-Coop

## 1. Objetivo

Desenvolver o projeto de forma coordenada, documentada, verificável e segura, utilizando múltiplas IAs com responsabilidades distintas.

## 2. Responsabilidades

### ChatGPT — Coordenador técnico

- Definir a arquitetura e as prioridades.
    
- Dividir objetivos em tarefas executáveis.
    
- Analisar os relatórios dos agentes.
    
- Avaliar resultados e propor próximos passos.
    
- Preparar materiais para revisão independente.
    
- Consolidar descobertas e decisões.
    
- Distinguir fatos, hipóteses e especulações.
    

### Cline — Agente principal de execução

- Analisar os arquivos do projeto.
    
- Investigar problemas técnicos.
    
- Implementar tarefas autorizadas.
    
- Executar testes autorizados.
    
- Produzir relatórios objetivos.
    
- Informar arquivos modificados e comandos executados.
    

### Codex — Especialista sob demanda

- Desenvolver implementações alternativas.
    
- Analisar problemas de programação complexos.
    
- Revisar código produzido pelo Cline.
    
- Investigar erros específicos.
    
- Comparar soluções técnicas.
    
- Participar quando solicitado pelo coordenador.
    

O Codex não precisa participar de todos os ciclos.

### Gemini Free — Auditor independente

- Avaliar propostas e conclusões.
    
- Questionar premissas.
    
- Identificar inconsistências.
    
- Examinar evidências e trechos de código.
    
- Apontar riscos e alternativas.
    
- Não assumir que o coordenador está correto.
    
- Não inventar problemas para justificar sua função.
    

O Gemini receberá relatórios e materiais selecionados, sem acesso direto aos arquivos do projeto.

## 3. Ciclo normal de desenvolvimento

1. ChatGPT define uma tarefa.
    
2. Cline investiga ou implementa.
    
3. Cline entrega um relatório.
    
4. ChatGPT analisa o resultado.
    
5. Gemini revisa propostas importantes.
    
6. ChatGPT avalia as críticas.
    
7. A solução é corrigida, testada ou aprovada.
    
8. As descobertas são documentadas.
    
9. Uma nova tarefa é iniciada.
    

## 4. Participação do Codex

O Codex será acionado quando:

- O Cline encontrar dificuldades técnicas.
    
- Uma implementação alternativa for necessária.
    
- Uma revisão independente de código puder reduzir riscos.
    
- Houver necessidade de comparar abordagens.
    
- O coordenador identificar uma tarefa adequada à ferramenta.
    

Evitar tarefas duplicadas sem justificativa técnica.

## 5. Integridade das informações

Toda informação técnica relevante deve ser classificada como:

- Fato confirmado por teste.
    
- Fato confirmado por código ou documentação.
    
- Hipótese fundamentada.
    
- Especulação.
    
- Informação desconhecida.
    

A concordância entre IAs nunca deve ser considerada prova.

Toda conclusão importante deve preservar sua origem e as evidências que a sustentam.

## 6. Segurança e autorização

Nenhum agente pode, sem autorização explícita:

- Instalar ferramentas ou dependências.
    
- Modificar arquivos do projeto.
    
- Compilar programas.
    
- Alterar configurações do PCSX2.
    
- Modificar a memória do jogo.
    
- Executar ações que alterem o estado do jogo.
    
- Apagar arquivos ou snapshots.
    

A autorização para uma ação não representa autorização permanente para ações futuras.

## 7. Qualidade dos relatórios

Toda tarefa deve registrar:

- Objetivo.
    
- Arquivos examinados.
    
- Métodos utilizados.
    
- Comandos executados.
    
- Resultados obtidos.
    
- Arquivos modificados.
    
- Erros encontrados.
    
- Limitações da investigação.
    
- Próximos passos sugeridos.
    

## 8. Preservação do projeto

- Manter cópias de segurança antes de alterações importantes.
    
- Preservar snapshots originais.
    
- Não sobrescrever evidências anteriores.
    
- Registrar mudanças relevantes.
    
- Manter documentação independente da memória das IAs.
    

## 9. Critério de conclusão

Uma tarefa só é considerada concluída quando seu resultado foi verificado por evidências ou testes compatíveis com o objetivo.

Uma implementação sem teste deve ser classificada como implementada, mas não validada.