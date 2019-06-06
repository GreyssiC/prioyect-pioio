# Proyecto 1 

Diseñamos y desarrollamos un programa que permita reproducir el juego Senku. Es un juego de tablero con una distribución dependiente del estilo que quieres jugar, inicialmente todos los espacios, representado por los vértices de los cuadrados, están ocupados, excepto el espacio central que se encuentra vacío, los espacios ocupados se representan por O y los espacios vacíos se representado por +.

_Elimina las piezas saltando sobre ellas con otra pieza adyacente. El juego acaba cuando sólo queda una._

## Requisitos 🚀

Trabajamos este código en el programa C++

### Pre-requisitos 📋
En el desarrollo de este código usamos variables estructuradas y arreglos. 
Generalmente:

**ARRAYS**

Donde cada elemento se almacena de forma consecutiva en memoria

```
void imprimir(char **matriz,int estilo){
    for (int i = 0; i < estilo; i++) {
        for (int j = 0; j < estilo; j++) {
            cout << matriz[i][j] << " ";
        }
        cout << endl;
    }
    cout<<endl;
}
```

**PUNTEROS**

Permiten simular el paso por referencia, crear y manipular estructuras dinamicas de datos, tales como listas enlazadas, pilas, colas y árboles. Existen dos operadores: operador de dirección (&) y operador de indirección (*)

```
Ejemplo con operador de indireción:
int validarficha(int f,int c,char **matriz){
    if(matriz[f][c]=='0'){
        return(1);
    }
    else{
        return(0);
    }
}
```

**MATRICES**

Es juna serie de vectores contenidos uno en el otro (u otros), es decir, es un vector cuyas posiciones son otros vectores

```
En este caso, ya estaban declaradas las matrices anteriormente:
void mover(int validm,int fichaf,int  fichac,int  movf,int movc,char **&matriz){
    char a;
    a=matriz[fichaf][fichac];
    matriz[fichaf][fichac]=matriz[movf][movc];
    matriz[movf][movc]=a;
    if (validm==1){
        matriz[fichaf+1][fichac]='+';
    }
    else if(validm==2){
        matriz[fichaf-1][fichac]='+';
    }
    else if(validm==3){
        matriz[fichaf][fichac+1]='+';
    }
    else if(validm==4){
        matriz[fichaf][fichac-1]='+';
    }
}
```

_No hemos usado ninguna librería que no venga dentro del C++_


### Instalación 🔧

_Una serie de ejemplos paso a paso que te dice lo que debes ejecutar para tener un entorno de desarrollo ejecutandose_

_Dí cómo será ese paso_

```
Da un ejemplo
```

_Y repite_

```
hasta finalizar
```

_Finaliza con un ejemplo de cómo obtener datos del sistema o como usarlos para una pequeña demo_

## Ejecutando las pruebas ⚙️

_Explica como ejecutar las pruebas automatizadas para este sistema_

### Analice las pruebas end-to-end 🔩

_Explica que verifican estas pruebas y por qué_

```
Da un ejemplo
```

### Y las pruebas de estilo de codificación ⌨️

_Explica que verifican estas pruebas y por qué_

```
Da un ejemplo
```
