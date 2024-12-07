# 1. Formulación del problema

<p align="center">
  <img src="image.png" alt="Imagen del ejercicio n°1" />
</p>

# 2. Resolución

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
