algoritmo "Controle_Acesso_Sala" em pseudocódgio

    var
      totalAlunosFila, i: inteiro
      alunoNaLista: logico
    
    inicio
      escreva("Digite a quantidade de alunos na fila: ")
      leia(totalAlunosFila)
      i = 1
  
      enquanto i <= totalAlunosFila faca
          escreva("Verificando aluno ", i, " de ", totalAlunosFila)
          
  
          escreva("O nome do aluno consta na lista? (verdadeiro/falso): ")
          leia(alunoNaLista)
  
  
          se alunoNaLista = verdadeiro entao
              escreva("Acesso Permitido. Seja bem-vindo(a)!")
          senao
              escreva("ERRO: Entrada Negada. Nome não consta na lista oficial.")
  
          i = i + 1
  
      escreva("Processo de entrada finalizado.")
