<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 5 


<!-- Su documentación aquí -->package com.mycompany.herencia1;

public class Herencia1 {
    //super(nombre,avitantes,can_de_departa);

    public static void main(String[] args) {

        colombia colombia1 = new colombia("Antioquia", "Medellin", 4000);

        colombia1.mostrarDatos();

    }

}



package com.mycompany.herencia1;

public class colombia extends pais {

    private String departamento;

    public colombia(String departamento, String nombre, int habitantes) {
        super(nombre, habitantes);
        this.departamento = departamento;
    }

    public void mostrarDatos() {
        System.out.println("Nombre: " + getNombre() + " Habitantes: " + getHabitantes() + " Departamento: " + departamento);
    }

}





package com.mycompany.herencia1;

public class pais {

    private String nombre;
    private int habitantes;

    public pais(String nombre, int habitantes) {
        this.nombre = nombre;
        this.habitantes = habitantes;
    }

    public String getNombre() {
        return nombre;
    }

    public int getHabitantes() {
        return habitantes;
    }

    public void setNombre(String nombre) {
        this.nombre = nombre;
    }

    public void setAvitantes(int avitantes) {
        this.habitantes = avitantes;
    }

}






