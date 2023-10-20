<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 10 


<!-- Su documentación aquí -->

```java
package com.mycompany.atividad10;


public class Atividad10 {

    public static void main(String[] args) {
        coche coche1 =new coche();
      coche1.unaaccion();
      
       biciclita bicicleta1 =new biciclita();
      bicicleta1.unaaccion();
      
      moto moto1 =new moto();
      moto1.unaaccion();
    }
}
package com.mycompany.atividad10;


public class Vehiculo {
   public void unaaccion(){
       System.out.println("el vehiculo ase una acion");
   }  
}



package com.mycompany.atividad10;


public class biciclita  extends Vehiculo {
    @Override
    public void unaaccion() {
        System.out.println("la bicicleta gira");
    }
}
package com.mycompany.atividad10;


public class coche  extends Vehiculo {
     @Override
    public void  unaaccion(){
        System.out.println("el coche frena");
    }
    

}

package com.mycompany.atividad10;


public class moto extends Vehiculo{
     @Override
    public void unaaccion() {
        System.out.println("la mota acelera");
    }
    
}
```
```java

package com.mycompany.poliformismoactvidad10_2;


public class Poliformismoactvidad10_2 {

    public static void main(String[] args) {
      cuenta cuentacorriente1 =new cuentacorriente();
      cuentacorriente1.makeSound();
      
      cuenta cuentadeahorro1 =new cuentadeahorro();
      cuentadeahorro1.makeSound();
    
       
       cuenta cuentaplazofijo1 =new cuentaplazofijo();
      cuentaplazofijo1.makeSound();
    }
}

package com.mycompany.poliformismoactvidad10_2;


public class cuenta {
 public void makeSound() {
        System.out.println("movencion de cuentas");
    }     
    
}

package com.mycompany.poliformismoactvidad10_2;


public class cuentacorriente extends cuenta {
 @Override
    public void makeSound() {
        System.out.println("retira dinero de la cuenta corriente()");
    }   
}

package com.mycompany.poliformismoactvidad10_2;


public class cuentadeahorro extends cuenta{
    
  @Override
    public void makeSound() {
        System.out.println(" depositar dinero en la cuenta de ahorro()");
       
    }    
}
package com.mycompany.poliformismoactvidad10_2;


public class cuentaplazofijo extends cuenta{
     public void makeSound() {
        System.out.println("counsultar saldo en la cuenta aplazo fijo()");
    } 
    
}
```
```java
package com.mycompany.poliformismoclse10_2;


public class Poliformismoclse10_2 {

    public static void main(String[] args) {
    producto libro1 =new libro();
      libro1.makeSound();
      
       producto CD_Y_DVD1 =new CD_Y_DVD();
      CD_Y_DVD1.makeSound();
    }
}

package com.mycompany.poliformismoclse10_2;


public class CD_Y_DVD extends producto{
    @Override
    public void makeSound() {
        System.out.println("calcular precio de los CD Y DVD()");
    }   
}

package com.mycompany.poliformismoclse10_2;


public class libro extends producto{
    @Override
    public void makeSound() {
        System.out.println("calcular impuesto de libro()");
    }   
    
}

package com.mycompany.poliformismoclse10_2;

public class producto {
   public void makeSound() {
        System.out.println("Calcular precios y puestos");
    }      
}

```