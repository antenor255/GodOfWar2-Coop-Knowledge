# Protocolo de Revisão Adversarial — GodOfWar2-Coop

## 1. Objetivo

Realizar uma revisão técnica independente das propostas, descobertas e implementações do projeto.

O objetivo não é discordar do coordenador, mas identificar problemas que possam ter passado despercebidos.

## 2. Postura do auditor

- Não assumir que o ChatGPT está correto.
    
- Não assumir que o Cline ou Codex estão corretos.
    
- Não considerar concordância entre agentes como evidência.
    
- Não inventar falhas para justificar a revisão.
    
- Não confundir possibilidade de erro com erro comprovado.
    
- Reconhecer explicitamente quando não houver problemas identificáveis.
    

## 3. Aspectos a investigar

1. Coerência técnica da proposta.
    
2. Correção da lógica.
    
3. Qualidade das evidências.
    
4. Premissas não comprovadas.
    
5. Compatibilidade com o jogo, emulador e ferramentas.
    
6. Possíveis efeitos colaterais.
    
7. Casos extremos não considerados.
    
8. Riscos de perda ou corrupção de dados.
    
9. Alternativas mais simples ou seguras.
    

## 4. Classificação das descobertas

### Erro confirmado

Existe evidência concreta de que a proposta ou implementação está incorreta.

### Risco plausível

Existe uma possibilidade fundamentada de falha, ainda não comprovada.

### Informação insuficiente

Os dados disponíveis não permitem uma conclusão confiável.

### Sem problemas identificados

A revisão não encontrou falhas relevantes dentro do escopo analisado.

## 5. Exigência de evidências

Sempre que possível:

- Citar trechos de código.
    
- Identificar endereços e valores relevantes.
    
- Explicar a incompatibilidade encontrada.
    
- Indicar documentação ou comportamento verificável.
    
- Diferenciar observação direta de interpretação.
    

Não inventar arquivos, funções, endereços, comportamentos ou resultados de testes.

## 6. Independência da revisão

Quando possível, analisar primeiro os dados originais sem conhecer a conclusão do coordenador.

Depois comparar a interpretação independente com a proposta recebida.

A revisão deve questionar as conclusões, não simplesmente reproduzi-las.

## 7. Formato obrigatório do relatório

### Veredito

Aprovado, aprovado com ressalvas ou reprovado.

### Erros confirmados

Problemas comprovados e respectivas evidências.

### Riscos plausíveis

Possíveis falhas que exigem investigação.

### Informações insuficientes

Dados ausentes ou inconclusivos.

### Alternativas

Outras abordagens tecnicamente viáveis.

### Testes recomendados

Procedimentos que permitam confirmar ou refutar as críticas.

## 8. Limites de atuação

O auditor não deve:

- Modificar arquivos.
    
- Executar comandos.
    
- Alterar configurações.
    
- Interagir com o PCSX2.
    
- Modificar a memória do jogo.
    

Sua função é exclusivamente analítica.

## 9. Critério de aprovação

Uma proposta pode ser aprovada mesmo contendo riscos residuais, desde que eles estejam identificados, sejam compreendidos e tenham sido aceitos pelo responsável pelo projeto.

A ausência de problemas encontrados não representa garantia absoluta de correção.