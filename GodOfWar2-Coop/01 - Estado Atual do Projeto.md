# Estado Atual do Projeto — GodOfWar2-Coop

## 1. Objetivo

Criar cooperação local em tela dividida para God of War II de PS2, permitindo controlar dois Kratos na mesma instância do PCSX2.

Objetivo técnico prioritário: investigar a possibilidade de renderizar um segundo modelo 3D de Kratos com transformação independente, mantendo uma única lógica de jogo, física e inimigos.

## 2. Ambiente

- Sistema: Windows 11
    
- Emulador: PCSX2 2.8.2
    
- Jogo: God of War II — SCUS-97481
    
- CRC: 2F123FD8
    
- Versão: 1.01
    
- ELF extraído: `game/SCUS_974.81`
    
- PINE: `127.0.0.1:28011`
    
- Workspace: `C:\Users\felip\Projects\GodOfWar2-Coop`
    

## 3. Estratégias investigadas

### A. Duplicação da estrutura do jogador

Região candidata: `0x003355A0`.

Vetor candidato: `0x003355C0`, com quatro valores float.

Em dois pares de snapshots, os componentes em `0x003355C0` e `0x003355C8` mudaram durante o movimento. Os componentes em `0x003355C4` e `0x003355CC` permaneceram iguais.

**Situação:** região candidata a conter coordenadas do jogador. Ainda não foi comprovado que seja a estrutura completa de Kratos nem que os componentes correspondam a eixos específicos.

### B. Duplicação da renderização

Grupos GS candidatos à renderização de Kratos:

- GS #065
    
- GS #066
    
- GS #067
    
- GS #068
    
- GS #069
    

O jogador confirmou que Kratos estava inteiro e claramente visível na captura usada para a identificação. Esses grupos serão tratados como candidatos operacionais à renderização do personagem.

**Limitação:** os grupos GS mostram dados após o processamento da geometria. Não revelam diretamente a matriz de transformação de mundo nem demonstram como duplicar o modelo em 3D.

## 4. Prioridade técnica atual

Investigar o pipeline de renderização anterior ao GS, especialmente onde a transformação 3D do modelo é aplicada.

Objetivo da investigação:

1. Identificar como o modelo de Kratos é enviado ao processamento vetorial.
    
2. Localizar a transformação aplicada ao modelo.
    
3. Verificar se é possível duplicar ou alterar essa transformação sem duplicar a lógica de jogo.
    
4. Determinar se uma segunda câmera independente é tecnicamente viável.
    

Não presumir que os grupos GS candidatos sejam suficientes para implementar a duplicação.

## 5. Análise do ELF

Informações confirmadas:

- ELF32 little-endian.
    
- Arquitetura MIPS.
    
- Entry point: `0x00100008`.
    
- Segmento PT_LOAD:
    
    - Endereço virtual inicial: `0x00100000`
        
    - Tamanho em arquivo: `0x001FBDA8`
        
    - Tamanho em memória: `0x0027FE00`
        

A região `0x003355xx` está dentro do espaço de memória do segmento, mas além dos dados presentes no arquivo. Isso é compatível com uma região BSS ou memória não inicializada no ELF.

Buscas por algumas formas diretas de referência a `0x003355C0` não encontraram correspondências. Isso não exclui referências indiretas ou construídas em tempo de execução.

## 6. Ferramentas de análise

- MSYS2 instalado em `C:\msys64`.
    
- PS2 toolchain oficial em investigação.
    
- Repositório `ps2toolchain-ee` clonado em `C:\ps2dev-src\ps2toolchain-ee`.
    
- Binutils oficial `ee-v2.45.1` clonado.
    
- Compilação de binutils ainda não concluída.
    
- Ambiente utilizado: MSYS2 MINGW32.
    
- Prefixo planejado: `ps2dev/ee`.
    

### Problema pendente

A compilação falha durante a criação das bibliotecas `libctf`:

`./libtool: line 1131: cd: null directory`

A investigação apontou que o comando de link tenta trabalhar com diretório de saída vazio, mas a causa ainda não foi identificada.

Um `make -n` executou receitas com prefixo `+`, apesar do modo de simulação, e criou `/libctf.a`. Não repetir esse comando.

**Próxima investigação:** verificar como o Libtool calcula `output_objdir`, `outputname` e os diretórios de saída durante o link das bibliotecas `libctf`.

Não apagar arquivos ou diretórios criados durante a compilação sem autorização.

## 7. Ferramentas e scripts do projeto

Local: `tools/`

- `pine_diag.ps1`
    
- `pine_snapshot.ps1`
    
- `pine_batch_test.ps1`
    
- `pine_diff.ps1`
    

Os scripts PINE permitem consultar e comparar regiões de memória do jogo.

**Restrição atual:** o jogo está fechado. Não executar scripts PINE nem reabrir o PCSX2 sem autorização explícita.

## 8. Estado de execução

- Nenhuma implementação de segundo jogador concluída.
    
- Nenhuma transformação independente de modelo comprovada.
    
- Nenhuma câmera independente implementada.
    
- Investigação estática do ELF em andamento.
    
- Compilação de binutils pendente de diagnóstico.
    

## 9. Restrições obrigatórias

- Não usar cheats.
    
- Não modificar a memória do jogo sem autorização.
    
- Não interagir com o PCSX2 nem reabrir o jogo sem autorização explícita.
    
- Não instalar dependências sem autorização específica.
    
- Não compilar sem autorização específica.
    
- Não modificar arquivos sem autorização.
    
- Não alterar PATH global, Registro, variáveis globais ou permissões sem autorização.
    
- Preservar snapshots e backups.
    
- Não tratar hipóteses como fatos.
    
- Não considerar concordância entre IAs como evidência.
    

## 10. Critério de validação

Uma descoberta só deve ser considerada confirmada quando houver evidência reproduzível, como:

- leitura ou escrita observada;
    
- instrução de código corretamente decodificada;
    
- relação entre endereço e comportamento demonstrada;
    
- teste controlado com resultado comparável;
    
- documentação técnica confiável.
    

Implementado não significa testado. Testado não significa validado.