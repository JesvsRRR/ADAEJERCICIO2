# 1. Formulación del problema

<p align="center">
  <img src="image.png" alt="Imagen del ejercicio n°2" />
</p>

# 2. Resolución

> I) Entrada del valor de la variable "dimension"
- Nuevamente se inicializa la libreria java  `"Scanner"` para ingresar datos.
- Se ingresa el valor numero entero a variable `"d"` que equivaldra a las dimensiones de la matriz cuadratica.
```bash
import java.util.Scanner;
```

```bash
    public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    System.out.println("Ingresar dimension [d]: ");
    int d = sc.nextInt();
    if(d <= 0){
        d = sc.nextInt();;
    }
```
> II) Ingreso de numeros enteros en la matriz en un rotación especifica

- Se llama a una función void `"Rotar(d)"` , la cual usara la vairable `"d"`.
- A continuación inicializa la `Matriz[d][d]` y se ingresan los valores numericos de la matriz por elemento, a diferencia del recorrido de esquina izquierda a derecha ([i][j]) se cambian los parametros del index de la matriz para ordenar los valores en 90° ([j][d - i - 1]).
```bash
    Rotar(d);
```

```bash
    public static void Rotar(int d){
    Scanner sc = new Scanner(System.in);    
    int[][] Matriz = new int[d][d];
    
    
    for(int i=0; i < d; i++){
        for(int j=0; j < d;j++){
            System.out.print("["+i+"]"+"[" + j+"]");
            Matriz[j][d - i - 1] = sc.nextInt();           
        }
    }
```

> III) Impresión de la matriz cuadrada original y la matriz cuadrada rotada

- Con la matriz rellena,se realizan dos bucles dobles para imprimir la matriz original y la matriz rotada.

```bash
    System.out.println("MATRIZ ORIGINAL: ");
    for(int i=0; i < d; i++){
        for(int j=0; j < d;j++){
            System.out.print("["+Matriz[j][d - i - 1]+"]");        
        }
    System.out.println("");    
    }
    
    System.out.println("MATRIZ ROTADA: ");
    for(int i=0; i < d; i++){
        for(int j=0; j < d;j++){
            System.out.print("["+Matriz[i][j]+"]");        
        }
    System.out.println("");    
    }
    }
```

### Codigo completo

```bash
import java.util.Scanner;

public class Main {

    public static void Rotar(int d){
    Scanner sc = new Scanner(System.in);    
    int[][] Matriz = new int[d][d];
    
    
    for(int i=0; i < d; i++){
        for(int j=0; j < d;j++){
            System.out.print("["+i+"]"+"[" + j+"]");
            Matriz[j][d - i - 1] = sc.nextInt();           
        }
    }

    System.out.println("MATRIZ ORIGINAL: ");
    for(int i=0; i < d; i++){
        for(int j=0; j < d;j++){
            System.out.print("["+Matriz[j][d - i - 1]+"]");        
        }
    System.out.println("");    
    }
    
    System.out.println("MATRIZ ROTADA: ");
    for(int i=0; i < d; i++){
        for(int j=0; j < d;j++){
            System.out.print("["+Matriz[i][j]+"]");        
        }
    System.out.println("");    
    }
    }

    
    public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    System.out.println("Ingresar dimension [d]: ");
    int d = sc.nextInt();
    if(d <= 0){
        d = sc.nextInt();;
    }
    
    Rotar(d);
        
         
    }
    
}
```
# 3. Complejidad

> I) Entrada del valor de la variable "dimension"

- Complejidad de tiempo: 𝑂(1) (el usuario puede ingresar valores inválidos repetidamente, pero cada entrada toma tiempo constante 𝑂(1))
- Complejidad de espacio: 𝑂(1) (No se utilizan estructuras adicionales, y el espacio ocupado por las variables locales y la libreria `Scanner` es constante)

> II) Ingreso de numeros enteros en la matriz en un rotación especifica 

- Complejidad de tiempo: 𝑂(d²)
- Complejidad de espacio: 𝑂(d²)
  - (Al tener una estructura bidimensional y bucles dobles que recorrer dichos formatos, la complejidad tiempo y espacio equivalen a 𝑂(d²))

> III) Impresión de la matriz cuadrada original y la matriz cuadrada rotada

- Complejidad de tiempo: 𝑂(d²) (Dominada por el recorrido completo de la matriz para imprimir y calcular la rotación)
- Complejidad de espacio: 𝑂(d²) (Dominada por el almacenamiento de las matrices original y rotada)


