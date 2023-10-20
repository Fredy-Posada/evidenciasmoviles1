<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 

```java
<!-- Su documentación aquí -->

package com.mycompany.actvidad8m;

import java.util.ArrayList;

public  class Actvidad8M {

    public static void main(String[] args) {
     ArrayList<Cancion> Canciones = new  ArrayList<>();
     
     Canciones.add(new Cancion("me ilucione","juan","binomio"));
     
     Canciones.add(new Cancion("sefue","pedro", "acaban de llegar"));
     Canciones.add(new Cancion("ya llego","frankin", "no estan aqui"));
     
     Album Album = new Album(Canciones);
     Album.play();
     Album.next();
     Album.stop();
        }
}
package com.mycompany.actvidad8m;
import java.util.ArrayList;

public class Album extends Musica{
    ArrayList<Cancion> Canciones = new  ArrayList<>();
private int index = 0;
Cancion CanCionatual;

    public Album(String titulo, ArrayList Canciones) {
        super(titulo);
        this.Canciones = Canciones;
        this.CanCionatual = this.Canciones.get(index);
    }

    

    @Override
    void play() {
     CanCionatual =  Canciones.get(index);
     CanCionatual.play();
    }

    @Override
    void stop() {
      CanCionatual.stop();
      CanCionatual.stop();
    }

    @Override
    void pause() {
     CanCionatual.pause();
        System.out.println("pause "+ this.getTitulo());
    }

    @Override
    void next() {
    if(index<Canciones.size())        
    this.index++;   
    }

    @Override
    void previous() {
    if (index > 0)
     this.index--;     
    }

    
    
        
    }
    
package com.mycompany.actvidad8m;




public class Cancion extends Musica{
    private String artista;
    private String Album;
    
    public Cancion(String artista, String Album, String titulo) {
        super(titulo);
        this.artista = artista;
        this.Album = Album;
    }
    
    

    @Override
    void play() {
        System.out.println("play " + this.getTitulo());
           }

    
    

    @Override
    void stop() {
      System.out.println("stop " + this.getTitulo());  
    }

    @Override
    void pause() {
     System.out.println("stop "+ this.getTitulo() );   
    }

    @Override
    void next() {
       
    }

    @Override
    void previous() {
      
    }
    

    

    public void setIndex(int index) {
       
    }

    
    
    
    
    
    
}

package com.mycompany.actvidad8m;

public abstract  class Musica {
    private String titulo;

    public Musica(String titulo) {
        this.titulo = titulo;
    }

    public String getTitulo() {
        return titulo;
    }

    public void setTitulo(String titulo) {
        this.titulo = titulo;
    }
    
    
    
    abstract void play();
    abstract void stop();
    abstract void pause();
    abstract void next();
    abstract void previous();

    

    
    
    
}
```