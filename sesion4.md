<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4


<!-- Su documentación aquí -->package producto;


public class Producto {
 // Atributos con distintos modificadores de acceso
    public String nombre;        
    private double precio;                
    final String fabricante;     
    static String marca;         
    String categoria;            
    protected int cantidad;
    // Constructor
    public Producto(String nombre, double precio, int cantidad, String marca,String fabricante, String categoria) {
        this.nombre = nombre;
        this.precio = precio;
        this.cantidad = cantidad;
        this.fabricante = fabricante;
        this.marca  =  marca;
        this.categoria = categoria;
    }

    // Getter y Setter para el atributo privado "precio"
    public double getPrecio() {
        return precio;
    }

    public void setPrecio(double precio) {
        this.precio = precio;
    }

    // Método toString() para representar el producto en forma de cadena
    
    public String toString() {
        return "Producto{" +
                "nombre='" + nombre + '\'' +
                ", precio=" + precio +
                ", cantidad=" + cantidad +
                ", fabricante='" + fabricante + '\'' +
                ", marca='" + marca + '\'' +
                ", categoría='" + categoria + '\'' +
                '}';
    }

    // Método main para probar la clase Producto
    public static void main(String[] args) {
        // Crear una instancia de Producto
        Producto producto = new Producto("arroz", 15.75, 25,"Diana", "Dicorp",  "alimento");

        // Acceder a los atributos utilizando los getters
        System.out.println("Nombre: " + producto.nombre);
        System.out.println("Precio: " + producto.getPrecio());
        System.out.println("Cantidad: " + producto.cantidad);
        System.out.println("Fabricante: " + producto.fabricante);
        
        System.out.println("Marca: " + Producto.marca);
        System.out.println("Categoría: " + producto.categoria);
  
        // Mostrar el producto actualizado
        System.out.println(producto);
    }
}
    
   
        
    
    








