<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 


<!-- Su documentación aquí -->
```java
package com.mycompany.activida8;


public class Activida8 {
 
    public static void main(String[] args) {
          
        System.out.println("nombre de la cancion!");
        System.out.println("nombre del album");
        System.out.println("nombre de la pelicula");
        System.out.println("");
    }
    
}
```
```java
package com.mycompany.activida8;


public class Album extends Musica{
    
    private String cancion;

    public Album(String cancion, String titulo) {
        super(titulo);
        this.cancion = cancion;
    }
    

      @Override
   public void play(){
          System.out.println("reproduce el album" );
          
   }
     @Override
   public void stop(){
         System.out.println("detiene la reproducción del album");
   }
    @Override
   public void pause(){
        System.out.println(" pausa la reproducción del album");
   }
    @Override
   public void next(){
        System.out.println("avanza al siguiente album");
   }
     @Override
   public void previous(){
         System.out.println("retrocede album");
   }
}
```
```java
package com.mycompany.activida8;


public class BandaSonora extends Musica {
   
    private String pelicula;

    public BandaSonora(String pelicula, String titulo) {
        super(titulo);
        this.pelicula = pelicula;
    }

  
  
    @Override
    public void play(){
        System.out.println("Reproduce la pelicula");
    }
   @Override
   public void stop(){
       System.out.println("para la pelicula" );
       
   }
   @Override
   public void pause(){
       System.out.println("pausa la pelicula");
       
   }
   @Override
   public void next(){
       System.out.println("avanza a la siguiente pelicula");
   }
   @Override
    public void previous(){
        System.out.println("retrocede a la pelicula anterior");
    }
   
    }   
    ```
```java
package com.mycompany.activida8;



public class Cancion extends Musica{

    private String artista;
    private String albun;

    public Cancion(String artista, String albun, String titulo) {
        super(titulo);
        this.artista = artista;
        this.albun = albun;
    }

   
   

    
    
    @Override
    public void play(){
        System.out.println("Reproduce la cancion");
    }
   @Override
   public void stop(){
       System.out.println("para la cacion");
       
   }
   @Override
   public void pause(){
       System.out.println("pausa la cancion");
       
   }
   @Override
   public void next(){
       System.out.println("avanza a la siguiente canción");
   }
   @Override
    public void previous(){
        System.out.println("retrocede a la canción anterior");
    
    }   
    
}
```
```java
package com.mycompany.activida8;


abstract public class Musica {
    private String titulo;
    
    public Musica(String titulo){
        this. titulo= titulo;
    }
    public abstract void play();
    public abstract void stop();
    public abstract void pause();
    public abstract void next();
    public abstract void previous();       
            
}

 ```   

   
    







