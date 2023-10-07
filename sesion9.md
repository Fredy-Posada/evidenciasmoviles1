<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 9 


<!-- Su documentación aquí -->
```java
package com.mycompany.appconversor.java;


public class AppconversorJava {

    public static void main(String[] args) {
        Temperatura t1 = new Temperatura("Celcius", "Fahrenheit");
        Temperatura t2 = new Temperatura("Fahrenheit", "Celcius");
        
        
        System.out.println(t1.convertir(30));
        
        System.out.println(t2.convertir(30));

    }
}


package com.mycompany.appconversor.java;


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
 ```   

```java
package com.mycompany.appconversor.java;


public class Longitud extends Conversor {

    public Longitud(String unidadOrigen, String unidadDestino) {
        super(unidadOrigen, unidadDestino);
    }
    

@Override
    public double convertir(double cantidad) {
        if (unidadOrigen.equals("metros") && unidadDestino.equals("pies")) {
            // metros a pies
            return cantidad * 3.281;
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

```



```java
package com.mycompany.appconversor.java;


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

```

```java
package com.mycompany.appconversor.java;


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
        } else if (unidadOrigen.equals("Gramos") && unidadDestino.equals(" Libras")) {
            // Gramos a Libras.
            return cantidad * 0.00220462;
        } else if (unidadOrigen.equals(" Libras") && unidadDestino.equals("Gramos")) {
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
            }else if (unidadOrigen.equals("Libras.") && unidadDestino.equals("Libras ")) {
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
```

```java
package com.mycompany.appconversor.java;


public class programador extends Conversor{

    public programador(String unidadOrigen, String unidadDestino) {
        super(unidadOrigen, unidadDestino);
        
    }
    
    
        System.out.println("Seleccione la conversión que desea realizar:");
        System.out.println("1. Decimal a Binario");
        System.out.println("2. Decimal a Hexadecimal");
        System.out.println("3. Binario a Decimal");
        System.out.println("4. Hexadecimal a Binario");

        int opcion = scanner.nextInt();

        switch (opcion) {
            case 1:
                System.out.print("Ingrese un número decimal: ");
                int decimal = scanner.nextInt();
                String binario = Programador.decimalABinario(decimal);
                System.out.println("Resultado: " + binario);
                break;
            case 2:
                System.out.print("Ingrese un número decimal: ");
                int decimal2 = scanner.nextInt();
                String hexadecimal = Programador.decimalAHexadecimal(decimal2);
                System.out.println("Resultado: " + hexadecimal);
                break;
            case 3:
                System.out.print("Ingrese un número binario: ");
                String binario2 = scanner.next();
                int decimal3 = Programador.binarioADecimal(binario2);
                System.out.println("Resultado: " + decimal3);
                break;
            case 4:
                System.out.print("Ingrese un número hexadecimal: ");
                String hexadecimal2 = scanner.next();
                String binario3 = Programador.hexadecimalABinario(hexadecimal2);
                System.out.println("Resultado: " + binario3);
                break;
            default:
                System.out.println("Opción no válida");
        }

        scanner.close();
    }
```

```java
class programador {
    public static String decimalABinario(int decimal) {
        return Integer.toBinaryString(decimal);
    }

    public static String decimalAHexadecimal(int decimal) {
        return Integer.toHexString(decimal);
    }

    public static int binarioADecimal(String binario) {
        return Integer.parseInt(binario, 2);
    }

    public static String hexadecimalABinario(String hexadecimal) {
        return Integer.toBinaryString(Integer.parseInt(hexadecimal, 16));
    }
}



package com.mycompany.appconversor.java;


public abstract class Conversor {
    protected String unidadOrigen;
    protected String unidadDestino;

    public Conversor(String unidadOrigen, String unidadDestino) {
        this.unidadOrigen = unidadOrigen;
        this.unidadDestino = unidadDestino;
    }
    
     public abstract double convertir(double cantidad);
}
```