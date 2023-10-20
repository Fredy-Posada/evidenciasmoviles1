<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 9 


<!-- Su documentación aquí -->
```java
package com.mycompany.app10;


public abstract class Conversor {
    protected String unidadOrigen;
    protected String unidadDestino;

    public Conversor(String unidadOrigen, String unidadDestino) {
        this.unidadOrigen = unidadOrigen;
        this.unidadDestino = unidadDestino;
    }
    
     public abstract double convertir(double cantidad);
}

package com.mycompany.app10;


public class Divisas extends Conversor{

    public Divisas(String unidadOrigen, String unidadDestino) {
        super(unidadOrigen, unidadDestino);
    }

   @Override
    public double convertir(double cantidad) { 
        if (unidadOrigen.equals("Dólar estadounidense") && unidadDestino.equals("Euro")) {
            // Dólar estadounidense a Euro.
            return cantidad  * 0.94;
            
        } else if (unidadOrigen.equals("Euro") && unidadDestino.equals("Dólar estadounidense")) {
            //Euro a Dólar estadounidense 
            return cantidad * 1.06;
            
        } else if (unidadOrigen.equals("Dólar estadounidense") && unidadDestino.equals("Peso colombiano")) {
            // Dólar estadounidense a Peso colombiano
            return cantidad * 4070.75;
            
        } else if (unidadOrigen.equals(" Peso colombiano") && unidadDestino.equals("Dólar estadounidense ")) {
            //Peso colombiano a Dólar estadounidense 
            return cantidad * 0.00025;
            
        } else if (unidadOrigen.equals("Euro") && unidadDestino.equals("Peso colombiano")) {
            // Euro a Peso colombiano
            
            return cantidad * 4301.64 ;
        } else if (unidadOrigen.equals(" Peso colombiano") && unidadDestino.equals("Euro")) {
            //  Peso colombiano a Euro 
           
             } else {
            }
             throw new IllegalArgumentException("Unidades de temperatura no compatibles");
        }
   

           
}
    

ackage com.mycompany.app10;


public class Longitud extends Conversor {

    public Longitud(String unidadOrigen, String unidadDestino) {
        super(unidadOrigen, unidadDestino);
    }
    

@Override
    public double convertir(double cantidad) {
        if (unidadOrigen.equals("metros") && unidadDestino.equals("pies")) {
            
            return 0.0;
        } else if (unidadOrigen.equals("pies") && unidadDestino.equals("metros")) {
            // pies a metros
            return cantidad * 0.3048;
        } else if (unidadOrigen.equals("kilometros") && unidadDestino.equals("millas")) {
            // kilometros a millas
            return cantidad * 0.6213;
        } else if (unidadOrigen.equals("millas") && unidadDestino.equals("kilometros")) {
            // millas a kilometros
            return cantidad * 1.60934;
        } else if (unidadOrigen.equals("centimetros") && unidadDestino.equals("pulgadas")) {
            //centimetros a pulgadas
            
            return cantidad *0.393701;
        } else if (unidadOrigen.equals("pulgadas") && unidadDestino.equals("centimetros")) {
            // pulgadas a centimetros
           
            return cantidad * 2.54;
        }else if (unidadOrigen.equals("yardas") && unidadDestino.equals("metros")) {
            // yardas a metros
           
            return cantidad * 0.9144;
            
            }else if (unidadOrigen.equals("metros") && unidadDestino.equals("yardas")) {
            // metros yardas 
           
            return cantidad * 1.09361;
             }else if (unidadOrigen.equals("Millas Náuticas.") && unidadDestino.equals("Kilómetros")) {
            // Millas Náuticasa a Kilómetros
           
            return cantidad * 1.852;
            }else if (unidadOrigen.equals("kilometros") && unidadDestino.equals("Millas Náuticas")) {
            // Kilómetros a Millas Náuticasa
           
            return cantidad * 0.539957;
            
            }else if (unidadOrigen.equals("Micrómetros ") && unidadDestino.equals(" Milímetros")) {
            // Micrómetros a Milímetros
           
            return cantidad * 0.001;
             }else if (unidadOrigen.equals("milimetros ") && unidadDestino.equals(" Micrómetros ")) {
            //  Milímetros a micrometros
           
            return cantidad * 1000;
             }else if (unidadOrigen.equals("Decímetros") && unidadDestino.equals(" Metros ")) {
            // Decímetros a Metros.
           
            return cantidad *0.1;
            }else if (unidadOrigen.equals("metros") && unidadDestino.equals(" Decímetros ")) {
            //  Metros a Decímetros 
           
            return cantidad *10;
            
             
              
        
               } else {   
            throw new IllegalArgumentException("Unidades de temperatura no compatibles");
        }
    }
}

package com.mycompany.app10;

public class Temperatura extends Conversor {

    public Temperatura(String unidadOrigen, String unidadDestino) {
        super(unidadOrigen, unidadDestino);
    }

    @Override
    public double convertir(double cantidad) {
        if (unidadOrigen.equals("Celsius") && unidadDestino.equals("Fahrenheit")) {
            // Celsius a Fahrenheit
            return (cantidad * 9 / 5) + 32;
        } else if (unidadOrigen.equals("Fahrenheit") && unidadDestino.equals("Celsius")) {
            // Fahrenheit a Celsius
            return (cantidad - 32) * 5 / 9;
        } else if (unidadOrigen.equals("Celsius") && unidadDestino.equals("Kelvin")) {
            // Celsius a Kelvin
            return cantidad + 273.15;
        } else if (unidadOrigen.equals("Kelvin") && unidadDestino.equals("Celsius")) {
            // Kelvin a Celsius
            return cantidad - 273.15;
        } else if (unidadOrigen.equals("Fahrenheit") && unidadDestino.equals("Kelvin")) {
            // Fahrenheit a Kelvin
            double celsius = (cantidad - 32) * 5 / 9;
            return celsius + 273.15;
        } else if (unidadOrigen.equals("Kelvin") && unidadDestino.equals("Fahrenheit")) {
            // Kelvin a Fahrenheit
            double celsius = cantidad - 273.15;
            return (celsius * 9 / 5) + 32;
        } else {
            throw new IllegalArgumentException("Unidades de temperatura no compatibles");
        }
    }
}

package com.mycompany.app10;


public class binario  extends Conversor{
    
  public binario(String unidadOrigen, String unidadDestino) {
        super(unidadOrigen, unidadDestino);
    }
 public String decimalToBinary(int decimalNumber) {
        return Integer.toBinaryString(decimalNumber);
    }

    public int binaryToDecimal(String binaryNumber) {
        return Integer.parseInt(binaryNumber, 2);
    }

    public String decimalToHexadecimal(int decimalNumber) {
        return Integer.toHexString(decimalNumber);
    }

    public int hexadecimalToDecimal(String hexadecimalNumber) {
        return Integer.parseInt(hexadecimalNumber, 16);
    }         
  
    @Override
    public double convertir(double cantidad) {
    if (unidadOrigen.equals("decimal") && unidadDestino.equals("binario")) {
            return Double.parseDouble(decimalToBinary((int) cantidad));
        } else if (unidadOrigen.equals("binario") && unidadDestino.equals("decimal")) {
            return binaryToDecimal(String.valueOf((int) cantidad));
        } else if (unidadOrigen.equals("decimal") && unidadDestino.equals("hexadecimal")) {
            return Double.parseDouble(decimalToHexadecimal((int) cantidad));
        } else if (unidadOrigen.equals("hexadecimal") && unidadDestino.equals("decimal")) {
            return hexadecimalToDecimal(String.valueOf((int) cantidad));
        } else {
            throw new IllegalArgumentException("Unidades de conversión no compatibles");
            
            
           
        }
     }

    }  


package com.mycompany.app10;


public class peso extends Conversor {

    public peso(String unidadOrigen, String unidadDestino) {
        super(unidadOrigen, unidadDestino);
    }
    @Override
    public double convertir(double cantidad) {
        if (unidadOrigen.equals("Kilogramos") && unidadDestino.equals("libras")) {
            // Kilogramos a Libras.
            return cantidad * 2.20462;
        } else if (unidadOrigen.equals("libras") && unidadDestino.equals("kilogramos")) {
            // libras a kilogramos
            return cantidad * 0.453592;
        } else if (unidadOrigen.equals("gramos") && unidadDestino.equals(" libras")) {
            // Gramos a Libras.
            return cantidad * 0.00220462;
        } else if (unidadOrigen.equals(" libras") && unidadDestino.equals("Gramos")) {
            // libras a gramos
            return cantidad * 453.592;
        } else if (unidadOrigen.equals("Kilogramos") && unidadDestino.equals("Gramos")) {
            //Kilogramos a Gramos.
            
            return cantidad * 1000;
        } else if (unidadOrigen.equals("Gramos") && unidadDestino.equals("Kilogramos")) {
            //  gramos a kilogramos 
           
            return cantidad * 0.001;
        }else if (unidadOrigen.equals("Toneladas") && unidadDestino.equals("Kilogramos.")) {
            // Toneladas a Kilogramos.
           
            return cantidad * 1000;
            
            }else if (unidadOrigen.equals("Kilogramos.") && unidadDestino.equals("Toneladas")) {
            // kilogramos a Toneladas
           
            return cantidad * 0.001;
             }else if (unidadOrigen.equals("Libras") && unidadDestino.equals("Onzas.")) {
            // Libras a Onzas.
           
            return cantidad * 16;
            }else if (unidadOrigen.equals("Onzas") && unidadDestino.equals("Libras")) {
            // onzas a libras
            
           
            return cantidad * 0.0625;
            
            }else if (unidadOrigen.equals("Gramos") && unidadDestino.equals("Onzas")) {
            // Gramos a Onzas
           
            return cantidad * 0.035274;
             }else if (unidadOrigen.equals("Onzas ") && unidadDestino.equals("Gramos")) {
            // onzas a gramos
           
            return cantidad * 28.3495;
             }else if (unidadOrigen.equals("Toneladas") && unidadDestino.equals("Libras.")) {
            // Toneladas a Libras.
           
            return cantidad * 2204.62;
            }else if (unidadOrigen.equals("Libras.") && unidadDestino.equals("Toneladas ")) {
            // libras a toneladas
           
            return cantidad * 0.00045359;
            
            }else if (unidadOrigen.equals("Toneladas") && unidadDestino.equals("Gramos")) {
            // Toneladas a Gramos
           
            return cantidad * 1e+6;
             }else if (unidadOrigen.equals("gramos") && unidadDestino.equals("toneladas")) {
            // gramos a toneladas
           
            return cantidad * 1e-6;
            
             }else if (unidadOrigen.equals("Toneladas") && unidadDestino.equals("Miligramos")) {
            // Toneladas a Miligramos
           
            return cantidad * 1e+9;
            }else if (unidadOrigen.equals("miligramos") && unidadDestino.equals("Toneladas")) {
            //  Miligramos a toneladas
           
            return cantidad * 1e-9;
             }else if (unidadOrigen.equals("Kilogramos") && unidadDestino.equals("Miligramos")) {
            //  Kilogramos a Miligramos
           
            return cantidad * 1e+6;
             }else if (unidadOrigen.equals("miligramos") && unidadDestino.equals("kilogramos")) {
            //  Miligramos a kilogramos
           
            return cantidad * 1e-6;
            
            
            
             
              
        
               } else {   
            throw new IllegalArgumentException("Unidades de temperatura no compatibles");
        }
    }
}

package com.mycompany.app10;

public class App10 {

    public static void main(String[] args) {
        System.out.println("  ");
        System.out.println("####TEMPERATURA#####   ");
        System.out.println("  ");
        Temperatura t1 = new Temperatura("Celsius", "Fahrenheit");
        Temperatura t2 = new Temperatura("Fahrenheit", "Celsius");
        Temperatura t3 = new Temperatura("Celsius", "Kelvin");
        Temperatura t4 = new Temperatura("Kelvin", "Celsius");
        Temperatura t5 = new Temperatura("Kelvin", "Fahrenheit");
        Temperatura t6 = new Temperatura("Fahrenheit", "Kelvin");

        double res = t1.convertir(2);

        System.out.println("de Celsius a Fahrenheit" + res);
        res = t1.convertir(2);
        System.out.println("de Celcius a Fahrenheit" + res);
        res = t2.convertir(10);
        System.out.println("de Fahrenheit a celcius" + res);
        res = t3.convertir(22);
        System.out.println("de Celcius a kelvin" + res);
        res = t4.convertir(32);
        System.out.println("Fahrenheit a kelvin" + res);
        res = t5.convertir(24);
        System.out.println("kelvin a Fahrenheit" + res);
        res = t6.convertir(25);
        System.out.println("Fahrenheit a kelvin" + res);
        
        System.out.println("  ");
        System.out.println("####LONGITUD#####   ");
        System.out.println("  ");
        
         Longitud t10 = new Longitud("metros", "pies");
        Longitud t11 = new Longitud("pies", "metros");
        Longitud t12 = new Longitud("kilometros", "millas");
        Longitud t13 = new Longitud("millas", "kilometros");
        Longitud t14 = new Longitud("centimetros", "pulgadas");
        Longitud t15 = new Longitud("pulgadas", "centimetros");
        Longitud t16 = new Longitud("yardas", "metros");
        Longitud t17 = new Longitud("metros", "yardas");
        
               
        res = t10.convertir(26);       
       System.out.println("metros a pies"+ res);
       res = t11.convertir(29);
       System.out.println("pies a metros"+ res);
       res = t12.convertir(23);
       System.out.println("kilometro a millas"+ res);
       res = t13.convertir(32);
       System.out.println("millas a kilometros"+ res);
       res = t14.convertir(42);
       System.out.println("centimetros a pulgadas"+ res);
       res = t15.convertir(52);
       System.out.println("pulgadas a centimetros"+ res);
       res = t16.convertir(62);
       System.out.println("yardas a metros"+ res);
       res = t17.convertir(32);
       System.out.println("metros a yardas "+ res);
       
        System.out.println("    ");
        System.out.println("  ");
        System.out.println("####PESO#####   ");
        System.out.println("  ");
        
        peso t24 = new peso("Kilogramos", "libras");
        res = t24.convertir(12);      
        System.out.println("kilogramos a libras" + res);
        
        peso t25 = new peso("libras", "kilogramos");
        res = t25.convertir(12);
        System.out.println("libras a kilogramos  "+ res);
        
         peso t26 = new peso("Kilogramos", "Gramos");
         res =t26.convertir(1);
         System.out.println(" kilogramos a gramosmo"+ res);
         
         peso t27 = new peso( "Gramos","Kilogramos");
         res =t27.convertir(1000);
         System.out.println(" Gramos a kilogramos"+ res);
         
        peso t28 = new peso("Onzas","Libras");
        res =t28.convertir(1000);
        System.out.println("onzas a libras"+ res);
        
        System.out.println("    ");
        System.out.println("####BINARIO#####   ");
        System.out.println("  ");
        
        binario t29 = new binario("decimal","binario");
        res = t29.convertir(200);
        System.out.println("decimal a binario"+ res);
        
       
        binario t32 = new binario("binario", "decimal");
        binario t33 = new binario("decimal", "hexadecimal");
        binario t34 = new binario("hexadecimal", "decimal");
        
        res = t32.convertir(100);
        System.out.println(" binario a decimal " + res);
        res = t33.convertir(50);
        System.out.println(" decimal a hexadecimal " + res);
        res = t34.convertir(20);
        System.out.println(" hexadecimal a decimal " + res);
        System.out.println("  ");
        System.out.println("####DIVISAS#####   ");
        System.out.println("  ");
        
        Divisas t35 = new  Divisas("Dólar estadounidense","Euro");
        Divisas t36 = new  Divisas("Euro","Dólar estadounidense");
        Divisas t37 = new  Divisas("Dólar estadounidense","Peso colombiano");
        Divisas t38 = new  Divisas("Euro","Dólar estadounidense");
        Divisas t39 = new  Divisas("Dólar estadounidense","Euro");
        Divisas t40 = new  Divisas("Euro","Peso colombiano");
         
        
       
        
        res = t35.convertir(25);
        System.out.println("dolar estaunidense a euro "+ res);
        res = t36.convertir(55);
        System.out.println("Euro a dolar estaunidense "+ res);
        res = t37.convertir(80);
        System.out.println("Dolar Estaunidense a Peso Colombiano " + res);
        
        res = t38.convertir(10);
        System.out.println("Euro a Dólar estadounidense "+ res);
        res = t39.convertir(40);
        System.out.println("Dólar estadounidense a Euro  "+ res);
        res = t40.convertir(24);
        System.out.println("Euro a peso colombiano "+ res);
       
        
                
        
         
    }
}
```