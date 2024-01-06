# Cadastro de Clientes - Exercício de Função/Procedimento 📋👥

Este é um exemplo de algoritmo simples em Portugol que realiza operações básicas de cadastro de clientes. O programa permite cadastrar, pesquisar, excluir e sair.

## Código Fonte 🖋️

```portugol
var
  opcaoMenu: literal
  clientes: vetor[1..5] de literal

procedimento mostrarMenu()
inicio
  Escreval("1-Cadastrar clientes")
  Escreval("2-Pesquisar")
  Escreval("3-Excluir")
  Escreval("4-Sair")
  leia(opcaoMenu)
fimprocedimento

procedimento cadastrar()
var
  i: inteiro
inicio
  para i de 1 ate 5 faca
    se clientes[i] = "" entao
      Escreval("Informe o nome do cliente: ")
      leia(clientes[i])
      interrompa
    fimse
  fimpara
fimprocedimento

procedimento pesquisar()
var
  nomePesquisar: literal
  i, indiceSucesso: inteiro
inicio
  indiceSucesso <- -1
  Escreval("Informe o nome a pesquisar: ")
  leia(nomePesquisar)
  para i de 1 ate 5 faca
    se clientes[i] = nomePesquisar entao
      indiceSucesso <- i
      interrompa
    fimse
  fimpara
  se indiceSucesso = -1 entao
    Escreval("Cliente não encontrado")
  senao
    Escreval("Cliente encontrado na posição ", indiceSucesso)
  fimse
fimprocedimento

procedimento excluir()
var
  indiceExclusao: inteiro
inicio
  Escreval("Informe o índice a excluir")
  leia(indiceExclusao)
  se (indiceExclusao > 5) ou (indiceExclusao < 1) entao
    escreval("Índice Inválido")
  senao
    clientes[indiceExclusao] <- ""
  fimse
fimprocedimento

inicio
  repita
    mostrarMenu()
    escolha opcaoMenu
      caso "1"
        cadastrar()
      caso "2"
        pesquisar()
      caso "3"
        excluir()
    fimescolha
  ate opcaoMenu = "4"
fimalgoritmo
```
# Melhorias no README 🌟

## Descrição do Projeto
Este projeto consiste em um algoritmo simples de cadastro de clientes desenvolvido na linguagem de programação Portugol. Ele oferece funcionalidades básicas, como cadastro, pesquisa, exclusão e saída.

## Instruções de Uso 🚀

1. **Execução do Programa:**
   - Certifique-se de ter um ambiente adequado para executar códigos em Portugol.
   - Copie o código fonte apresentado acima.
   - Execute o código em um interpretador ou compilador Portugol.

2. **Funcionalidades:**
   - Ao iniciar, o programa exibirá um menu com opções numeradas de 1 a 4.
   - Escolha a opção desejada digitando o número correspondente.
   - Para cadastrar um cliente, selecione a opção "1" e siga as instruções.
   - Para pesquisar um cliente, escolha a opção "2" e forneça o nome a ser pesquisado.
   - Para excluir um cliente, selecione a opção "3" e informe o índice do cliente a ser removido.
   - Para sair do programa, escolha a opção "4".

## Observações ℹ️

- O programa permite o cadastro de até 5 clientes.
- Os clientes são armazenados em um vetor de strings.
- Certifique-se de seguir as instruções apresentadas no console durante a execução.

Esperamos que este projeto seja útil para entender conceitos básicos de programação procedural e manipulação de vetores em Portugol.


