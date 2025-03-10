	La programación dinámica es un método de programación que busca reducir el 
	tiempo de ejecución de un algoritmo.

Ésta fue creada por el matemático Richard Bellman, y cuyo enfoque consiste en dividir un problema grande y complejo en problemas más pequeños y simples. El conjunto de solución de los problemas pequeños resuelve en su conjunto al problema mayor.

<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTw1kg38VmuA6hKlx8DQ9yTJUEUWz8D43y3Jg&s">

Un ejemplo de esto sería una solución, aplicando programación dinámica, a la secuencia de los números de Fibonacci, donde tenemos la siguiente secuencia:

$$
 F_{0} = 1
$$
$$
 F_{1} = 1
$$
$$ 
F_{n} = F_{n-1} + F_{n-2}\  \forall n \geq 2 
$$
Una de las formas para resolver el problema descrito es mediante de forma iterativa, un ejemplo de ello es el siguiente:

```c
#include <stdio.h>

void main(void)
{
	int x,y,z,cont;
	
	x=0;
	y=1;
	
	printf("0\n1\n");
	
	for (cont=1;cont<=20;cont=cont+1)
	{
		z=x+y;
		printf("%d\n", z);
		x=y;
		y=z;
	}
}
```

Ahora podemos ver el problema resuelto de forma recursiva:

```c
#include <stdio.h>

int fibonacci(int n)
{
	if n(>2):
		return fibonacci(n-1) + fibonacci(n-2);
	else if (n==2):
		return 1;
	else if (n==1):
		return 1;
	else if (n==0):
		return 0;
}

int main(void)
{
	int num;
	
	for (num=0; num<=20; num++)
	{
		printf("%d\n", fibonacci(num));
	}
	
	return 0;
}
```

Como podemos visualizar, la [[Recursividad|recursividad]] es una manera más sencilla de resolver el problema.