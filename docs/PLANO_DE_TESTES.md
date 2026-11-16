# Plano de testes — Elgin i9

Este documento é um roteiro para registrar os testes do projeto. Ele não é um programa de teste e não substitui os exemplos oficiais do professor.

## Antes de testar

- [ ] Conferir o modelo da impressora: Elgin i9.
- [ ] Conferir se o computador e o projeto estão configurados para 64 bits.
- [ ] Conferir a versão correta da DLL `E1_Impressora01.dll`.
- [ ] Conferir os arquivos XML de exemplo fornecidos pelo professor.
- [ ] Verificar papel, energia, cabo e conexão da impressora.
- [ ] Compilar o projeto e registrar qualquer erro antes do teste físico.

**Atenção:** não marque um teste como realizado apenas porque o código foi escrito ou compilado. O teste físico exige executar a função com a impressora conectada.

## Parâmetros indicados no enunciado

Use estes parâmetros de referência ao conferir o código e executar os testes:

| Recurso | Chamada/valores do professor |
|---|---|
| Conexão USB | tipo `1`, modelo `i9`, conexão `USB`, parâmetro `0` |
| Texto | `ImpressaoTexto(texto, 1, 4, 0)`; retorno não negativo indica sucesso; depois `Corte(5)` |
| QR Code | `ImpressaoQRCode(dados, 6, 4)`; depois `Corte(5)` |
| Código de barras | `ImpressaoCodigoBarras(8, "{A012345678912", 100, 2, 3)`; depois `Corte(5)` |
| XML SAT | `ImprimeXMLSAT(dadosXML, 0)`; liberar `dadosXML` com `free()` |
| Cancelamento SAT | `ImprimeXMLCancelamentoSAT(dadosXML, ASS_QRCODE, 0)`; liberar `dadosXML` com `free()` |
| Gaveta Elgin | `AbreGavetaElgin(1, 50, 50)` |
| Gaveta (outro comando) | `AbreGaveta(1, 5, 10)` |
| Sinal sonoro | `SinalSonoro(4, 50, 5)` |

Os comandos em geral indicam sucesso com retorno `0`. A exceção descrita no PDF é `ImpressaoTexto`, em que o erro é indicado por retorno negativo.

## Teste 1 — Inicialização e conexão da impressora

**Objetivo:** verificar se o programa carrega a biblioteca, configura os parâmetros e consegue abrir e fechar a conexão.

Procedimento:
1. Iniciar o programa.
2. Escolher a opção de configuração da conexão.
3. Informar os parâmetros solicitados pelo programa, conforme o material do professor.
4. Solicitar a abertura da conexão.
5. Conferir a mensagem e o valor de retorno.
6. Fechar a conexão e conferir o resultado.

Resultado:
- Data:
- Computador utilizado:
- Impressora conectada?:
- Resultado (aprovado/reprovado/não executado):
- Mensagem ou erro observado:
- Responsável:

## Teste 2 — Impressão de texto

**Objetivo:** verificar a impressão de um texto simples.

Procedimento:
1. Abrir a conexão com a impressora.
2. Escolher a função de impressão de texto.
3. Informar um texto curto de teste, sem dados pessoais.
4. Conferir se o texto foi impresso e se o retorno foi tratado corretamente.

Resultado:
- Resultado:
- Texto de teste:
- Observações:

## Teste 3 — Impressão de QR Code

**Objetivo:** verificar a geração e impressão de um QR Code.

Procedimento:
1. Abrir a conexão.
2. Escolher a opção de QR Code.
3. Informar um conteúdo de teste não sensível.
4. Conferir a impressão e, se possível, ler o QR Code com um celular.

Resultado:
- Resultado:
- O QR Code foi impresso?:
- Foi possível ler?:
- Observações:

## Teste 4 — Impressão de código de barras

**Objetivo:** verificar a impressão do código de barras previsto no trabalho.

Procedimento:
1. Abrir a conexão.
2. Escolher a opção de código de barras.
3. Usar somente os dados de teste definidos pela equipe ou pelo professor.
4. Conferir a impressão e a legibilidade.

Resultado:
- Resultado:
- Tipo/formato utilizado:
- Foi possível ler?:
- Observações:

## Teste 5 — Impressão do XML SAT

**Objetivo:** verificar a leitura do arquivo XML de teste e o envio para impressão SAT.

Procedimento:
1. Confirmar que o XML SAT oficial/de teste está no caminho esperado pelo programa.
2. Abrir a conexão.
3. Escolher a opção de impressão SAT.
4. Conferir se o arquivo foi aberto, se a função retornou sucesso e se houve impressão.
5. Conferir se a memória alocada para o conteúdo do XML foi liberada mesmo em caso de erro, conforme o fluxo implementado.

Resultado:
- Nome do arquivo utilizado:
- Resultado:
- Houve impressão física?:
- Observações:

## Teste 6 — Cancelamento SAT

**Objetivo:** verificar a função de impressão do XML de cancelamento SAT usando o arquivo de teste apropriado.

Procedimento:
1. Confirmar que o XML de cancelamento é um arquivo de teste fornecido/autorizado pelo professor.
2. Abrir a conexão.
3. Escolher a opção de cancelamento SAT.
4. Conferir o retorno da função e a impressão.
5. Conferir a liberação da memória do XML.

**Importante:** este teste é de impressão/processamento do documento de cancelamento conforme a atividade. Não faça cancelamentos fiscais reais usando dados de terceiros.

Resultado:
- Nome do arquivo utilizado:
- Resultado:
- Houve impressão física?:
- Observações:

## Teste 7 — Abertura da gaveta

**Objetivo:** testar separadamente os dois comandos de abertura da gaveta exigidos no trabalho.

- [ ] Testar o primeiro comando.
- [ ] Testar o segundo comando.

Resultado:
- Primeiro comando:
- Segundo comando:
- Observações:

## Teste 8 — Sinal sonoro

**Objetivo:** verificar se o comando de sinal sonoro é executado.

Procedimento:
1. Abrir a conexão.
2. Selecionar a opção de sinal sonoro.
3. Verificar se a impressora emite o sinal esperado.

Resultado:
- Resultado:
- O sinal foi ouvido?:
- Observações:

## Teste 9 — Proteção com conexão fechada

**Objetivo:** garantir que o programa não solicite dados de impressão nem execute operações de impressão quando a conexão estiver fechada.

Procedimento:
1. Iniciar o programa sem abrir a conexão ou fechar uma conexão já aberta.
2. Selecionar cada opção de impressão.
3. Conferir se o programa informa que a conexão está fechada e retorna sem pedir conteúdo/XML.

Resultado:
- Resultado:
- Opções verificadas:
- Observações:

## Resumo dos testes

| Teste | Status |
|---|---|
| Inicialização e conexão | Não executado |
| Texto | Não executado |
| QR Code | Não executado |
| Código de barras | Não executado |
| XML SAT | Não executado |
| Cancelamento SAT | Não executado |
| Gaveta — comando 1 | Não executado |
| Gaveta — comando 2 | Não executado |
| Sinal sonoro | Não executado |
| Operações com conexão fechada | Não executado |

Atualize os status somente depois de realizar cada teste. Registre separadamente compilação bem-sucedida e teste físico.
