# Estrutura do projeto

## Objetivo

Organizar os materiais do trabalho escolar de controle de uma impressora térmica Elgin i9 em C.

## Arquivos e pastas

```text
Projeto_Impressora_Elgin/
├── .gitignore
├── README.md
├── main.c
└── docs/
    ├── ARQUIVOS_NECESSARIOS.md
    ├── COMO_USAR_O_REPOSITORIO.md
    ├── ESTRUTURA_DO_PROJETO.md
    └── PLANO_DE_TESTES.md
```

## Sobre o main.c

O arquivo `main.c` presente neste momento é apenas um marcador de organização. Ele ainda não contém a implementação do programa. A equipe deve substituí-lo pelo código real, usando o código-base e as assinaturas oficiais fornecidas pelo professor.

Não inventar protótipos, typedefs, parâmetros ou nomes de funções da DLL. Conferir tudo no material original.

## Requisitos funcionais a acompanhar

- Login com até três tentativas.
- Menu em laço com opções 1 a 11 e 0 para sair.
- Configuração, abertura e fechamento da conexão.
- Impressão de texto, QR Code e código de barras.
- Impressão de XML SAT e de XML de cancelamento SAT.
- Abertura da gaveta pelos dois comandos exigidos.
- Sinal sonoro.
- Bloqueio de operações de impressão quando a conexão estiver fechada.
- Verificação dos valores de retorno.
- Liberação da memória usada para carregar XML.

## O que ainda depende dos materiais oficiais

A implementação do código, os protótipos e parâmetros da DLL, os nomes/caminhos exatos dos XMLs e os procedimentos finais de compilação devem ser conferidos com o PDF, o código e os exemplos entregues pelo professor.
