# Arquivos necessários ao projeto

Este documento registra os materiais recebidos do professor e onde cada um deve ficar. O enunciado concentra o programa em um único arquivo `main.c`; a DLL e os dois XMLs de teste ficam na pasta de execução.

## Materiais recebidos

| Material | Recebido? | Uso e local |
|---|---:|---|
| `Trabalho_C_Impressora.pdf` | Sim | Enunciado oficial; consultar durante o desenvolvimento. Pode ser colocado em `docs/` se for permitido compartilhar. |
| `main.c` | Sim | Código-base do professor, preenchido conforme as tarefas do PDF. Fica na raiz. |
| `XMLSAT.xml` | Sim | XML de teste da opção 7. Fica na raiz/pasta de execução. |
| `CANC_SAT.xml` | Sim | XML de teste da opção 8. Fica na raiz/pasta de execução. |
| `E1_Impressora01.dll` | Sim | DLL avulsa recebida, identificada como x64. Fica localmente na pasta de execução. |
| `Bibliotecas E1 Impressora.zip` | Sim | Pacote com DLLs nas pastas `x64/` e `x86/`. |

## Sobre a DLL e o ZIP

A DLL é uma biblioteca binária de terceiros. Não se deve presumir que pode ser redistribuída publicamente. Mantenha a DLL e o ZIP localmente e confirme com o professor antes de publicá-los no GitHub.

A DLL avulsa recebida foi identificada pelo cabeçalho PE como **64 bits (x64)**. O ZIP contém:
- `x64/E1_Impressora01.dll`
- `x86/E1_Impressora01.dll`

A arquitetura da DLL precisa combinar com a do compilador. Para o ambiente 64 bits definido pela equipe, use a DLL x64.

## Estrutura de execução

```text
Projeto_Impressora_Elgin/
├── main.c
├── E1_Impressora01.dll
├── XMLSAT.xml
└── CANC_SAT.xml
```

A pasta `docs/` guarda documentação; ela não substitui os arquivos que o programa procura na pasta de execução. O código procura os XMLs e a DLL pelo nome informado.
