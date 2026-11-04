# Protocolo de Comunicação entre Agentes

## 1. Objetivo

Padronizar a comunicação entre ChatGPT, Cline, Gemini e Codex durante o desenvolvimento do GodOfWar2-Coop.

Cada agente deve receber apenas o contexto necessário para sua função, sem depender de suposições ou de informações não verificadas.

## 2. Envio de tarefas ao Cline

Toda tarefa deve conter:

- Identificador da tarefa.
    
- Objetivo específico.
    
- Contexto técnico necessário.
    
- Arquivos ou regiões relevantes.
    
- O que deve ser investigado.
    
- O que não deve ser feito.
    
- Autorizações disponíveis.
    
- Resultado esperado.
    

O Cline deve investigar primeiro e apresentar um plano antes de executar ações que alterem o projeto.

## 3. Retorno do Cline

O relatório deve seguir o `Modelo de Relatório de Execução`.

Deve incluir:

- Arquivos examinados.
    
- Ferramentas utilizadas.
    
- Comandos executados.
    
- Evidências coletadas.
    
- Resultados observados.
    
- Interpretações e hipóteses.
    
- Arquivos modificados.
    
- Erros e limitações.
    
- Próximas ações sugeridas.
    

Se nenhuma alteração foi feita, declarar explicitamente.

## 4. Revisão pelo Gemini

O Gemini recebe um pacote contendo:

- Objetivo da tarefa.
    
- Proposta ou conclusão do Cline.
    
- Evidências relevantes.
    
- Trechos de código ou logs necessários.
    
- Limitações conhecidas.
    

Sempre que possível, enviar primeiro as evidências sem revelar a conclusão do Cline, permitindo uma análise independente.

O Gemini deve seguir o `Modelo de Revisão do Gemini`.

## 5. Avaliação do ChatGPT

O ChatGPT deve:

1. Comparar o relatório com o objetivo original.
    
2. Verificar se as evidências sustentam as conclusões.
    
3. Avaliar a revisão do Gemini.
    
4. Identificar divergências entre os agentes.
    
5. Separar erros confirmados de riscos e dúvidas.
    
6. Definir o próximo passo.
    
7. Solicitar autorização quando necessária.
    

A concordância entre agentes não substitui testes.

## 6. Uso do Codex

O Codex será acionado apenas quando necessário.

Casos adequados:

- Revisão independente de código.
    
- Investigação de erros complexos.
    
- Comparação de implementações.
    
- Avaliação de alternativas técnicas.
    
- Problemas que o Cline não conseguiu resolver.
    

O Codex não deve executar alterações sem autorização específica.

## 7. Regras de comunicação

- Não omitir evidências contrárias à própria conclusão.
    
- Não apresentar hipóteses como fatos.
    
- Não inventar resultados de testes.
    
- Não esconder erros ou limitações.
    
- Não modificar o escopo da tarefa silenciosamente.
    
- Não executar ações além da autorização recebida.
    
- Não considerar uma tarefa concluída apenas porque o código foi escrito.
    

## 8. Encerramento de uma tarefa

Uma tarefa só pode ser encerrada quando:

- O objetivo foi avaliado.
    
- O resultado foi documentado.
    
- As evidências foram preservadas.
    
- As limitações foram registradas.
    
- O estado da tarefa foi atualizado na fila.
    
- As decisões relevantes foram registradas.