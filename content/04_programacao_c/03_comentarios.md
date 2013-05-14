
## Comentários

Comentários servem como uma documentação básica de código descrevendo uma determinada funcionalidade. Os comentários são ignorados pelo compilador e servem exclusivamente para auxiliar o programador na manutenção do código. A linguagem C possui duas formas de adicionar comentários. É possível adicionar comentários de um única linha e comentários de múltiplas linhas. 

Para adicionar comentários de uma única linha é utilizada "//" (duas barras) no início da linha correspondente ao comentário. 

```c
#include <stdio.h>
int main(int argc, const char * argv[])
{
  //Este é um comentário de uma única linha
}
```

Para efetuar um comentário de múltiplas linhas é adicionado */\** para iniciar o bloco de comentário e *\*/* para finalizar o bloco. Todo o texto que estiver entre */\** e *\*/* será reconhecido como um comentário e ignorado pelo compilador.

```c
#include <stdio.h>
int main(int argc, const char * argv[])
{
  /* 
  Este é um bloco de texto
  contendo múltiplas linhas 
  de comentário.
  */
}
```

