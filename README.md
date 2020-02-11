# Algoritmos-aula-2

February 11th, 2020

1 - Aritmética
  Operações entre valores do tipo numérico, que têm como resultado um valor numérico
  *Operadores: +, -, *, /, %;
  
2 - Relacional
  Operações de comparação entre dois valores do mesmo tipo, que tem como resultado um valor lógico.
  * Operadores:
  == Igual            != Diferente
   > Maior             < Menor
  >= Maior ou igual   <= Menor ou igual
  
ex: 
   Expressão    |   Resultado
    5 >= 1      |      1(V)
   "ab"=="Ab"   |      0(V)  - Maiusculo é diferenciado de minúsculo
                |
                |
                
     PS: 2 variáveis: 4 combinações V ou F
     PS: n variáveis, 2 elevado a n combinações
       
3 - Lógica
  Um valor lógico pode estar apenas em um de dois estados: verdadeiro ou falso
  *Operadores:
  && (e): Se algum estado for falso, então falso
  ||(ou): Se algum estado for verdadeiro, então veradeiro
  !(não): Troca o estado
  
  Na linguagem C, um operando terá valor verdadeiro se for diferente de zero e o valor falso se for igual a zero.
  verdadeiro !=0
  falso = 0
  ex: Sejam a = 5, b="xyz" e c = 1
    Expressão                |  Resultado
     !(a==5)                 |    0(F)
     (b=="xyz") && c         |    !=0(V)
     (a==4)||(!c)            |    0(F)
       F      F
       
    Constante x Variável
*Conceito de constante*
  Uma constante é um valor fixo que não se modifica ao longo do tempo durante a execução do programa.
  Uma constante pode ser de qualquer um dos tipos primitivos de dados.
  
*Declaração de constantes*
  #define NOMEDACONSTANTE valor
  
  ex: 
  #define PI 3.1415
  #define NOTA_MIN_APROV 7.0
  #define CURSO "informatica"

*Conceito de variável*
  Uma variável é o nome de uma posição de memória onde se pode guardar qualquer valor de um tipo associado.
  Cada variável corresponde a uma posição de memória, cujo valor pode variar ao longo do tempo da execução do programa.
  O tipo da variável é o seu domínio, ou seja, ele define o conjunto de valores possíveis de serem armazenados na variável, bem como o conjunto de operadores que podem agir sobre a mesma.
  
*Declaração de variáveis:"
  É feita a associação do nome escolhido (identificador), com a respectiva posição de memória que o mesmo possa simbolizar. Além disso é indicado o tipo(domínio) daquela variável
  ex:
  Endereço | Nome da variável | tipo | conteúdo
  
  
  
  ex: float nota1, nota2;
      int totalu;
      char disciplina[30]
      
     
      Formatação de identificadores
  Um identificador de constante ou variável é formado po um ou mais caracteres alfa-numéricos(letras, números e underline), sendo que o primeiro caractere deve ser obrigatoriamente uma letra.
  Não pode haver espaçõ entre os caracteres
  ex: 
        Identificador válido           | Identificador inválido
              total                    |      3arquivo
         UmNomeMuitoComprido           |      casa 121 
             lado2                     |      x + y
           duas_palavras               |
              l123                     |
                                       
      

   
  
