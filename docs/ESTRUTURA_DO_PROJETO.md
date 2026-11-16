# Estrutura do projeto

## Organização do repositório

O enunciado determina que o programa fique em um único arquivo C, `main.c`. Os dois XMLs de teste também precisam ficar na raiz/pasta de execução.

```text
Projeto_Impressora_Elgin/
├── .gitignore
├── README.md
├── main.c
├── XMLSAT.xml
├── CANC_SAT.xml
└── docs/
    ├── ARQUIVOS_NECESSARIOS.md
    ├── COMO_USAR_O_REPOSITORIO.md
    ├── ESTRUTURA_DO_PROJETO.md
    └── PLANO_DE_TESTES.md
```

A DLL `E1_Impressora01.dll` também deve ficar na pasta de execução no computador usado para testar. Ela não aparece obrigatoriamente na árvore pública porque é uma biblioteca binária de terceiros e sua redistribuição precisa ser autorizada.

## Função de cada item
- `main.c`: programa em C, com login, menu, comunicação com a DLL e funções de impressão.
- `XMLSAT.xml`: dados de demonstração para impressão SAT.
- `CANC_SAT.xml`: dados de demonstração para impressão do cancelamento SAT.
- `E1_Impressora01.dll`: biblioteca da Elgin necessária em tempo de execução; manter localmente e usar a arquitetura correta.
- `README.md`: objetivo, requisitos, login, menu e instruções de execução.
- `docs/`: documentos de orientação e registro dos testes.

## Regra dos caminhos

O programa abre `XMLSAT.xml`, `CANC_SAT.xml` e `E1_Impressora01.dll` pelo nome. Portanto, esses arquivos precisam estar no diretório de trabalho usado ao executar o programa. Não basta deixá-los dentro de `docs/`.

## Estado
O `main.c` foi preenchido a partir do código-base e das orientações do PDF. A equipe ainda precisa compilar no Dev-C++ de 64 bits e testar cada comando com a impressora física. A verificação de sintaxe não comprova funcionamento do hardware.
