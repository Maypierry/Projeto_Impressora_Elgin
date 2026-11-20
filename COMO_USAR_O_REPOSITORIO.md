# Como usar este repositório

Este guia explica como a equipe pode compartilhar o projeto entre computadores usando GitHub.

## Acessar o projeto

Repositório: https://github.com/Maypierry/Projeto_Impressora_Elgin

Qualquer pessoa pode visualizar e baixar um repositório público. Para enviar alterações, a pessoa precisa ter permissão de escrita ou trabalhar por fork e pull request.

## Baixar o projeto pelo navegador

1. Abra o endereço do repositório.
2. Clique no botão **Code**.
3. Escolha **Download ZIP**.
4. Extraia o ZIP em uma pasta do computador.

## Trabalhar em mais de um computador com Git

Na primeira vez em cada computador:
1. Instale o Git, se necessário.
2. Abra o terminal na pasta em que deseja guardar o projeto.
3. Execute:

```bash
git clone https://github.com/Maypierry/Projeto_Impressora_Elgin.git
```

Antes de começar a trabalhar em um computador que já tem uma cópia:
1. Abra o terminal dentro da pasta do projeto.
2. Execute:

```bash
git pull
```

Depois de alterar arquivos:
1. Confira o que mudou:

```bash
git status
```

2. Prepare as alterações:

```bash
git add .
```

3. Registre um commit com uma mensagem clara:

```bash
git commit -m "Descreva a alteração realizada"
```

4. Envie ao GitHub:

```bash
git push
```

Antes de sair de um computador, faça commit e push das alterações que deseja continuar em casa. No outro computador, faça pull antes de editar.

## Colaboração

- Combine com a equipe quem está editando cada arquivo.
- Evite duas pessoas alterarem o mesmo `main.c` ao mesmo tempo.
- Não sobrescreva alterações dos colegas sem conversar.
- Use mensagens de commit que expliquem o que foi feito.
- Não coloque senhas, tokens ou dados pessoais no repositório.
- Confira a permissão de redistribuição da DLL antes de publicá-la.

## Observação sobre o repositório público

A visibilidade pública permite que outras pessoas leiam e baixem o conteúdo. Isso não dá automaticamente permissão para qualquer pessoa enviar alterações diretamente. Para editar a branch principal, é necessário ter permissão de escrita.
