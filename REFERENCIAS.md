# Referencias e decisoes de implementacao

## Projeto de referencia indicado pela equipe

- Repositorio: [Lucas Libano — sistema-impressora-elgin-c](https://github.com/LucasLibano/sistema-impressora-elgin-c)
- Arquivo consultado: `elgin-printer-main/projeto.c`
- O projeto foi usado como referencia para a organizacao das funcoes de comunicacao, impressao e menu.

## Material que prevalece

O comportamento final foi ajustado ao enunciado e ao codigo-base fornecidos pelo professor:

- O programa permanece concentrado em um unico `main.c`.
- O menu usa as opcoes 1 a 11 e 0 para sair.
- As opcoes 1 e 2 configuram e abrem a conexao.
- O login usa `admin` / `1234`, com no maximo tres tentativas.
- Os arquivos XML sao lidos como conteudo pela funcao `lerArquivo()`; nao se envia um caminho de arquivo no lugar do XML.
- Os parametros de comandos seguem os exemplos do PDF do trabalho, inclusive os dois comandos de gaveta.

## Adaptacoes importantes em relacao ao projeto de referencia

Durante a revisao do arquivo `projeto.c` do repositorio de referencia, foram identificados pontos que nao poderiam ser copiados literalmente para este trabalho:

1. **Estado da conexao:** a variavel de conexao do exemplo de referencia tem uso invertido em partes do fluxo. Neste projeto, `conexaoAberta = 0` significa fechada e `conexaoAberta = 1` significa aberta.
2. **XML SAT:** o enunciado fornece `lerArquivo()` e exige o envio do conteudo do XML. Por isso, o programa le `XMLSAT.xml` e `CANC_SAT.xml` para a memoria e libera a memoria com `free()` depois da chamada.
3. **Impressao de texto:** o PDF determina que retorno negativo e erro; retorno zero ou positivo e tratado como envio bem-sucedido.
4. **Convencao de chamada:** os ponteiros de funcao da DLL usam `WINAPI`, adequado a chamada Windows indicada pela API.
5. **Protecao das operacoes:** cada funcao de impressao ou acessorio verifica a conexao antes de solicitar dados ou chamar a DLL.
6. **Retorno e corte:** os retornos dos comandos e do corte sao verificados; o corte so e solicitado quando a operacao de impressao retorna sucesso.

## Limites da verificacao

A revisao do codigo e a comparacao com os materiais nao substituem a compilacao no Dev-C++ 64 bits nem o teste com a impressora Elgin i9 fisica. Nenhum teste fisico e declarado como aprovado neste documento. A equipe deve registrar os resultados em [PLANO_DE_TESTES.md](PLANO_DE_TESTES.md).
