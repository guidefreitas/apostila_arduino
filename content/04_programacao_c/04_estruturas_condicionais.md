## Estruturas Condicionais

As estuturas condicionais possibilitam desviar o fluxo de execução de um programa de acordo com um determindo critério. Veremos abaixo algumas alternativas fornecidas pela linguagem C para controlar o fluxo do programa.

### IF

A instrução *if* fornecida pela linguagem C permite executar uma porção de código quando a condição especificada for satisfeita. A condição para execução do bloco de código deve ser especificada entre *(* e *)* e pode conter diversas sentenças utilizando os operadores booleanos < (menor), > (maior), == (igual), != (diferente). 

```c
#include <stdio.h>
int main(int argc, const char * argv[])
{
  int idade = 0;
  printf("Digite sua idade: ");
  scanf("%d", &idade);
  if(idade < 18){
    printf("Esta pessoa é menor de idade.");
  }
}
```

Neste exemplo declaramos uma variável chamada *idade* e atribuímos a ela o valor 16. Em seguida utilizamos a estrutura condicional *if* para verificar se a idade é menor do que 18 e imprimir a mensagem.


### IF e ELSE

Além de executar um bloco de código quando a condição especificada no *if* é satisfeita existem situações onde é necessário realizar alguma outra ação quando a condição não é satisfeita.

```c
#include <stdio.h>
int main(int argc, const char * argv[])
{
  int idade = 0;
  printf("Digite sua idade: ");
  scanf("%d", &idade);
  if(idade < 18){
    printf("Esta pessoa é menor de idade.");
  }else{
    printf("Esta pessoa é maior de idade.");
  }
}
```

No exemplo acima utilizamos a cláusula *else* para especificar um bloco de código que será executado apenas quando a condição de *idade < 18* (idade menor que 18) não for satisfeita. Neste caso o programa imprimirá a mensagem "Esta pessoa é maior de idade" caso a variável idade possuir um valor 18 ou superior.

Caso seja necessário tomar uma ação de acordo com mais de uma condição, é possível utilizar o *if* seguido de um *else if* e por fim *else* para especificar a quatidade de condições necessárias para realizar a tarefa.

```c
#include <stdio.h>
int main(int argc, const char * argv[])
{
  int idade = 0;
  printf("Digite sua idade: ");
  scanf("%d", &idade);
  if(idade > 18){
    printf("Esta pessoa é maior de idade.");
  } else if (idade < 10){
    printf("Esta pessoa tem menos de 10 anos");
  } else {
    printf("Esta pessoa tem entre 10 e 18 anos.");
  }
}
```

No exemplo anterior são especificadas duas condições, na primeira se a idade for maior do que 18 anos e na segunda se a idade for menor do que 10 anos. Se nenhuma das condições forem satisfeitas o programa executará o bloco de código que consta dentro do *else*.

### Switch

Existem situações onde queremos identificar uma possibilidade diante de diversas alternativas. Neste caso podemos utilizar vários *if* e *else* porém essa prática resulta em um código extenso e repetitivo. Quando a quantidade de alternativas for muito grande é possível utilizar o *switch* para simplificar o processo de decisão.

```c
#include <stdio.h>
int main(int argc, const char * argv[])
{
    int comando = 0;
    printf("Selecione um dos comandos: \n");
    printf("1 - Imprimir\n");
    printf("2 - Calcular Total\n");
    scanf("%i", &comando);
    switch(comando){
        case 1 : printf("Comando imprimir selecionado\n");
            break;
        case 2 : printf("Comando calcular selecionado\n");
            break;
        default : printf("Comando inválido.");
            break;
    }
    return 0;
}
```

