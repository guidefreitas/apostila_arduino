## Estruturas Condicionais

As estuturas condicionais possibilitam desviar o fluxo de execução de um programa de acordo com um determindo critério. Veremos abaixo algumas alternativas fornecidas pela linguagem C para controlar o fluxo do programa.

### IF

A instrução *if* fornecida pela linguagem C permite executar uma porção de código quando a condição especificada for satisfeita. A condição para execução do bloco de código deve ser especificada entre *(* e *)* e pode conter diversas sentenças utilizando os operadores booleanos < (menor), > (maior), == (igual), != (diferente). 

```c
int idade = 16;
if(idade < 18){
  printf("Esta pessoa é menor de idade.");
}
```

Neste exemplo declaramos uma variável chamada *idade* e atribuímos a ela o valor 16. Em seguida utilizamos a estrutura condicional *if* para verificar se a idade é menor do que 18 e imprimir a mensagem.

### IF e ELSE

Além de executar um bloco de código quando a condição especificada no *if* é satisfeita existem situações onde é necessário realizar alguma outra ação quando a condição não é satisfeita.

```c
int idade = 16;
if(idade < 18){
  printf("Esta pessoa é menor de idade.");
}else{
  printf("Esta pessoa é maior de idade.");
}
```

No exemplo acima utilizamos a cláusula *else* para especificar um bloco de código que será executado apenas quando a condição de *idade < 18* (idade menor que 18) não for satisfeita. Neste caso o programa imprimirá a mensagem "Esta pessoa é maior de idade" caso a variável idade possuir um valor 18 ou superior.


### Switch
