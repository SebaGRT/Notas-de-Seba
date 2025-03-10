Podemos entender a los Tipos de Datos Abstractos, también conocidos como TDA, como un [[Dato]] que se le ve asociado a una función.
Esto quiere decir que podemos ver a un TDA como una [[Primitiva|primitiva]] + operaciones

**Ex.**
```c
#include <stdio.h>
void main(){
	int a[100];
	a[1] = 1000;
	printf("%d", a[1]);
}
```

En este ejemplo se tiene un arreglo definido de 100 elementos tipo int, que cuenta con la función de almacenar, extraer y avanzar por la estructura definida.

**Ex.**
```c
#include <stdio.h>
void main(){
int *a;
int n;
printf("Ingrese un numero: ");
scanf("%d", &n);
ptr = (int*)malloc(n*sizeof(int));
}
```

En el anterior ejemplo podemos visualizar una implementación similar al primer ejemplo, pero sin utilizar un TDA formato arreglo para su realización, y con estos podemos distinguirlos entre dos tipos.

###### TDA Estático
	Son estructuras de datos cuyo tamaño se determina en tiempo de compilación 
	(programación), la estructura es de tamaño fijo y nunca cambia. Ejemplos 
	incluyen arrays y structs. Se gestionan en la pila de memoria.

###### TDA Dinámico
	Su tamaño se determina en tiempo de ejecución, la estructura es de tamaño 
	variable y puede cambiar, utilizando memoria dinámica. Ejemplos son listas 
	enlazadas, pilas y colas. Requieren una gestión cuidadosa de la memoria 
	para evitar fugas.

