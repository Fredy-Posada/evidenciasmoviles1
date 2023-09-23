<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 1 


<!-- Su documentación aquí -->


# A first-level heading
## A second-level heading
### A third-level heading


Puede crear bloques de código delimitados colocando comillas simples triples ``` antes y después del bloque de código. Te recomendamos dejar una línea en blanco antes y después de los bloques de código para facilitar la lectura del formato sin procesar.

```java
package fredy.posadayarce;

import java.util.Scanner;

public class FredyPosadayarce {

    public static void main(String[] args) {

        Scanner lea = new Scanner(System.in);

        int n, i, meda, moda;

        String nom;

        float din;

        System.out.println("digite cuantos participantes :");

        n = lea.nextInt();

        for (i = 1; i <= n; i++) {

            System.out.println("digite el nombre del participante :" + i + ":");
            nom = lea.next();

            System.out.println("digite modalidad    (1= CARRERAS, 2= POLO ACUATICO, 3= CLAVADOS, 4=NATACION ARTISTICA):");

            moda = lea.nextInt();

            System.out.println("digite cuantas medallas :");
            meda = lea.nextInt();

            System.out.println("");

            if (meda == '1') {
                din = meda * 300000;

            } else {
                if (moda == '2') {
                    din = meda * 2000000;
                } else {
                    if (moda == '3') {
                        din = meda * 500000;
                    } else {
                        if (moda == '4') {
                            din = meda * 1000000;
                        } else {
                            System.out.println("asy no es es 1 al 4");

                        }
                    }
                }
            }

            din = meda * moda;
            System.out.println("%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%");
            System.out.println("         participante:" + nom);
            System.out.println("       cantidad de medallas:  " + meda);
            System.out.println("       cuantas medallasganadas:" + din);
            System.out.println("%%%%%%%%%%%%%%%%%%%%");

        }

    }

}

```






