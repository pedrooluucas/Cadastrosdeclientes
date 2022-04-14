# Cadastrosdeclientes

algoritmo "Exercícios Função/Procedimento"


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
          se clientes[i] = ""  entao
            Escreval("Informe o nome do clinete: ")
            leia(clientes[i])
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
            Escreval("Cliente encontrado na posição ",indiceSucesso)
       fimse
       



 fimprocedimento
 
  procedimento Excluir()
 var

    indiceExclusao : inteiro


 inicio

       Escreval("Informe o indice a excluir")
       leia(indiceExclusao)
       se(indiceExclusao > 5) ou (indiceExclusao < 1) entao
          escreval("Indice Inválido")
       senao
            clientes[indiceExclusao] <- ""
      fimse

 fimprocedimento



 
inicio

repita
     MostrarMenu()
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

