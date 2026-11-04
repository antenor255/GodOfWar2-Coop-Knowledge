# GodOfWar2-Coop

## Objetivo

Desenvolver uma experiência cooperativa local em tela dividida para God of War II (PS2), utilizando uma única instância do PCSX2.

O objetivo é permitir que dois jogadores controlem versões independentes de Kratos no mesmo mundo.

Não se trata de netplay nem de executar duas instâncias do emulador.

## Ambiente técnico

- Sistema: Windows 11.
    
- Emulador: PCSX2 2.8.2.
    
- Jogo: God of War II (PS2).
    
- Serial: SCUS-97481.
    
- CRC: 2F123FD8.
    
- Versão do jogo: 1.01.
    
- ELF extraído: `game/SCUS_974.81`.
    
- Comunicação com o PCSX2: PINE.
    

## Estratégias de investigação

### Estratégia A — Duplicação do jogador

Investigar a estrutura de memória do Kratos e descobrir quais dados precisam ser duplicados para permitir dois jogadores independentes.

### Estratégia B — Duplicação da renderização

Investigar a possibilidade de renderizar um segundo Kratos em 3D, com transformação e câmera independentes, mantendo uma única lógica de jogo, física e sistema de inimigos.

Esta é a linha de investigação prioritária.

## Descobertas importantes

- A região `0x003355C0` contém valores que mudam durante o movimento.
    
- Dois componentes dessa região variaram em diferentes pares de snapshots.
    
- Isso é compatível com dados de posição, mas ainda não comprova a propriedade ou a função exata da estrutura.
    
- Os grupos GS #065–#069 de uma captura foram identificados operacionalmente como candidatos à renderização do Kratos.
    
- Os dados GS mostram informações de desenho, mas não revelam diretamente a transformação de mundo aplicada antes da renderização.
    

## Ferramentas

- PCSX2 e interface PINE.
    
- Python e biblioteca zstandard.
    
- Scripts de diagnóstico, captura e comparação de memória na pasta `tools`.
    
- MSYS2 e toolchain PS2DEV em investigação.
    
- Cline e Codex para análise e implementação.
    

## Restrições

- Não utilizar cheats para modificar o comportamento do jogo.
    
- Não alterar a memória do jogo sem autorização.
    
- Não reabrir ou interagir com o PCSX2 sem autorização explícita.
    
- Não modificar arquivos sem autorização.
    
- Não transformar hipóteses em fatos sem testes.
    
- Preservar snapshots e relatórios originais.
    

## Próxima prioridade

Investigar o pipeline de renderização 3D e encontrar onde a transformação do modelo do Kratos é aplicada, antes de os vértices chegarem ao GS.

## Critério de sucesso

Dois jogadores controláveis, cada um com seu próprio Kratos, sem duplicar desnecessariamente a lógica do jogo, com possibilidade de câmeras independentes.
Teste de sincronização automática — 03/11/2026.
