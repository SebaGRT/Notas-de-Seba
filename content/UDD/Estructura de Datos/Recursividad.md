	Es una técnica de programación que consiste en que un segmento de código 
	se invoque a sí mismo.

En programación, se llama como método recursivo a las funciones que se llaman a sí mismas.

```c
void fn(int n){
	fn(n+1);
	printf("%d\n", n);
}
```

Existen ciertas reglas a la hora de utilizar/hacer funciones recursivas, algunas de ellas:
- Toda función tiene que tener una condición que detenga las llamadas recursivas, esto se llama **condición de borde**.
- La función tiene que realizar alguna acción con los datos.
Las llamadas recursivas no entregan resultados inmediatamente, ya que el primer paso es un proceso de almacenamiento de las llamadas conocido como "[[Empilamiento|empilamiento]]".
Cuando no hay más llamadas se comienza a resolver el problema desde la ultima llamada a la primera.

Aquí podemos ver el proceso con empilamiento:
```c
#include <stdio.h>

int fn(int n)
{

	if (n<=5) { //condición de borde
		fn(n+1); //llamada recursiva
		printf("%d\n", n); //proceso
	}
}

int main(void)
{

	return fn(1);
}
```

La llamada fn(n+1) se guarda en una memoria llamada [[Stack (Pila)|Stack]].

![[Stack-img.png]]

Cuando se encuentra una llamada recursiva, se guarda una copia del código en el [[Stack (Pila)|Stack]].
Cuando ya no hay más llamadas se procede a continuar con el resto del código de la llamada.

Un ejemplo que nos ayuda a entender la recursividad son las torres de hanoi. Se tienen 3 postes y el juego consiste en mover un grupo de discos de la torre A a la torre C.

Reglas:
- Solo se puede mover ar el disco que se encuentre arriba en cada poste.
- Un disco de mayor tamaño no puede estar sobre uno más pequeño que él mismo
- Solo se puede desplazar el disco que se encuentre arriba en cada poste.

<img src="https://cdn.kastatic.org/ka-perseus-images/5b5fb2670c9a185b2666637461e40c805fcc9ea5.png">

```c
#include <stdio.h>

int num=0;

void hanoi(int n,int inic,int tmp, int final){
	if(n==1){
	printf("\nMueva el disco i de la base %c a la base %c",inic, tmp);
	num++;
		return;
	}
	hanoi(n-1,inic,final,tmp);
	printf("\nMover el disco %d de la base %c a la base %c",n,inic,tmp);
	num++;
	hanoi(n-1,final,tmp,inic)
}

int main(){
	int n;
	printf("Digite el numero de discos : ");
	scanf("%d",&n);
	printf("Los movimientos para resolver la torre de hanoi son : ");
	hanoi(n,'A','C','B');
	printf("\n %d", num);
	return 0;
}
```

