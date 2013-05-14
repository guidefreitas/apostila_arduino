
## Imprimindo e lendo do console/terminal

Aplicações simples escritas em diversas linguagens utilizam o terminal para ler dados digitados pelo usuário ou para imprimir os resultados dos programas. Nesta seção vamos aprender a como imprimir e ler valores do terminal, como formatar esses dados de acordo com o seu tipo para uma correta manipulação no programa. 

### Imprimindo no console

Para imprimir valores no terminal é utilizado o comando *printf*. Este comando pode imprimir texto e o valor de variáveis formatando-as corretamente para exibição no console.

```c
#include <stdio.h>
int main(int argc, const char * argv[])
{
  printf("Olá mundo!");
}
```

Neste primeiro exemplo nosso programa imprime a frase *Olá mundo!* no terminal. Mas e se quisermos imprimir os valores das variáveis do nosso programa? Neste caso utilizaremos alguns comandos especiais para informar para a função *printf* qual é o tipo de variável que estamos trabalhando e assim, conseguir formatar corretamente no formato de texto.

```c
#include <stdio.h>
int main(int argc, const char * argv[])
{
  int idade = 18;
  printf("A variável idade tem o valor %d", idade);
}
```

O programa acima imprime a frase *A variável idade tem o valor 18*. Repare no símbolo *%d* passado no lugar onde queremos imprimir o valor da variável. Este símbolo diz para a função *printf* que o tipo da variável que vamos especificar é um inteiro. Após especificar a string com a frase que queremos imprimir contendo o lugar onde a variável deverá ser inserida precisamos passar qual é a variável que vai ser colocada no lugar do *%d*, é então passada a variável *idade* após a vírgula.

```c
#include <stdio.h>
int main(int argc, const char * argv[])
{
  int idade = 18;
  char nome[50] = "João";
  printf("Meu nome é %s e eu tenho %d anos", nome, idade);
}
```

Quando queremos passar mais de uma variável na mesma chamada da função *printf* especificamos os lugares onde elas deverão aparecer no texto e em seguida especificamos o nome das variáveis após a vírgula de acordo com a ordem em que aparecem no texto. Repare no exemplo acima, nele passamos duas variáveis, o nome e a idade. Repare também que o tipo da variável *nome* é diferente. Criamos uma vetor de *char* para armazenar o nome e portanto o tipo *%s* é especificado na chamada da função *printf*. Abaixo consta uma tabela contendo alguns dos símbolos possível a serem especificados na função *printf* e *scanf* (que usaremos a seguir).

| Símbolo    | Tipo de dado                     |
| -----------|:--------------------------------:| 
| %i         | Inteiros                         |
| %d         | Decimais ou Inteiros             |
| %f         | Floats                           |
| %c         | Caracter                         |
| %s         | Array de char (ou strings)       |
| %p         | Endereço de memória de ponteiros | 

### Lendo valores do console

Um programa normalmente não servirá apenas para imprimir valores. Normalmente é necessário também possibilitar que o usuário do programa possa digitar dados para serem inseridos no programa e determinar a sua execução. Para capturar e armazenar um dado digitado pelo usuário em uma variável utilizamos o comando *scanf*.

```c
#include <stdio.h>
int main(int argc, const char * argv[])
{
  char nome[50];
  printf("Por favor digite seu nome: ");
  scanf("%s", &nome);
  printf("Olá, %s.", nome);
}
```

Neste programa perguntamos qual é o nome do usuário e armazenamos na variável *nome*. Repare no símbolo *&s* especificado na função *scanf*, ele é responsável por dizer para a função que o dado que vamos receber do usuário é uma string e armazená-lo corretamente na variável especificada após a vírgula, no nosso caso, a variável nome. O símbolo especificado segue as mesmas regras da tabela mostrada na seção anterior do *print*f.

```c
#include <stdio.h>
int main(int argc, const char * argv[])
{
  int idade;
  char nome[50];
  printf("Por favor digite seu nome: ");
  scanf("%s", &nome);
  printf("Por favor digite sua idade: ");
  scanf("%i", &idade);
  printf("Olá, %s. Você tem %i anos", nome, idade);
}
```

Mais um exemplo, dessa vez perguntando e armazenando também a idade do usuário.






