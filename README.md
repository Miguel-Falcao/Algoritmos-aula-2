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
  Uma constante pode ser de qualquer um dos tipos primitivos de dados. (O usuário não consegue definir o valor da constante)
  Definir com letras maiúsculas
  
*Declaração de constantes*
  #define NOMEDACONSTANTE valor
  
  ex: 
  #define PI 3.1415
  #define NOTA_MIN_APROV 7.0
  #define CURSO "informatica"

*Conceito de variável*
  Uma variável é o nome de uma posição de memória onde se pode guardar qualquer valor de um tipo associado.
  Cada variável corresponde a uma posição de memória, cujo valor pode variar ao longo do tempo da execução do programa.
  Definir com letras minusculas
  O tipo da variável é o seu domínio, ou seja, ele define o conjunto de valores possíveis de serem armazenados na variável, bem como o conjunto de operadores que podem agir sobre a mesma.
  
*Declaração de variáveis:"
  É feita a associação do nome escolhido (identificador), com a respectiva posição de memória que o mesmo possa simbolizar. Além disso é indicado o tipo(domínio) daquela variável
  ex:
  Endereço | Nome da variável | tipo | conteúdo
   0010            nota1       float      9.8
   Não podemos associar ao endereço, pq ele pode estar ocupado por uma instrução do S.O. e isso travaria a máquina.

  ex: float nota1, nota2;
      int totalu;
      char disciplina[30]; Essa cadeia na verdade tem 29 espaços a serem preenchidos, o último posssui o \0
      
     
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
                                       
      Operações básicas
Operação de atribuição
  Especifica que uma variável recebe determinado valor, o qual deve ser de um tipo compatível com o valor da variável.
  Indicada pelo símbolo =
 Cuidado:
      = é usado para atribuição
     == é usado para comparação
 ex: Sejam a e b variáveis do tipo int.
 
 Operação | a  | b
  a = 2;  | 2  | ?
  b = a;  | 2  | 2
  a=a+3;  | 5  | 2
  b=a+b;  | 5  | 7

EM C:
  a=a+3; <-> a+=3;
  b=b-4; <-> b-=4
  c=c*2; <-> c*=2;
  d=d/5; <-> d/=5;
  
Operadores de Incremento e Decremento
  A linguagem C fornece dois operadores não usuais para incrementar e decrementar variáveis
  *Operador de incremento ++(soma 1 ao seu operando)
  *Operador de decremento --(subrai 1 do seu operando)
  
  ex:
    i++; incrementa i antes de usar seu valor
        -> são equivalentes a i=i+1
    ++i; incrementa i após usar o seu valor
    
    i--; decrementa i antes de usar seu valor
         -> são equivalentes a i=i+1
    --i; decrementa i após usar o seu valor
  
 ex:
  i = 5;
  x = i++;
  Qual o valor de x? R: 5
    
  i= 5;
  x = ++i; 
  Qual o valor de x? R: 6
  
   
 int a,b,x;      | a   | b   | x
  a = 5;         | 5   | ?   | ?
  b=5;           | 5   | 5   | ?
  x=a+b;         | 5   | 5   | 10
  x=a++ +b;      | 6   | 5   | 10
  x=++a +b;      | 7   | 5   | 12
  x=--a + b;     | 6   | 5   | 11
  x=a-- +b;      | 5   | 5   | 10
  x=a+b;         | 5   | 5   | 10

Bibliotecas em C:
  Para utilizarmos funções pré-definidas  na linguagem C, precisamos especificar em que lugar essas funções se encontram.
  Em C as funções estão armazenadas em bibliotecas e para utilizar essas funções precisamos informar em qual biblioteca elas se encontram.
  Para utilizarmos funções matemáticas (<math.h>) que contém as funções sin(), cos(),...
  Para utilizarmos funções de entrada e saída temos que declarar a biblioteca <stdio.h> que contém funções de leitura e escrita.
  
  Para fazer referência às bibliotecas deve-se declarar o arquivo em que se encontra a biblioteca.
  ex:#include<math.h> 
     #include<stdio.h>
     }
     Forma geral:
     printf("controle,arg1,arg2,...");
     printf() converte, formata e imprime argumentos na saída padrão sob o controle da cadeia de controle.
     A cadeia de controle contém dois tipos de objetos: Caracteres ordinários que são simplesmente copiados para o fluxo de saída, e especificações de conversão, cada uma causando a conversão e impressão no próximo argumento sucessivo do printf();
     Cada especificação de conversão é introduzida pelo caractere % e encerrado com um caractere de conversão.
     Os principais caracteres de conversão são:
     %d - O argumento é convertido para notação decimal
     %c - O argumento é um único caracter
     %s - O argumento é uma cadeia de caracteres
     %f - O argumento é tomado como um float ou double(Notação decimal)
     %e - O argumento é tomado como um float ou double(Notação Científica)
     
     Entrada formatada - scanf()
     
     forma geral:
     scanf("controle, arg1, arg2");
Estrutura básica de um programa em C

Declaração de constantes se houver
Declaração de variáveis se houver
main(){
  comandos;
}

     
     
  
    
    

   
  
