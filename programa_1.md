```mermaid
classDiagram
    class Hotel {
        -string nombre
        -vector <Habitacion> habitaciones 
        -vector <Cliente*> clientes
        +~Hotel()
        +void agregarHabitacion(int, string)
        +void registrarCliente(Cliente* cliente)
        +void mostrarInfo()
    }
    
    class Cliente {
        -int id
        -string nombre
        +Cliente(int, string)
        +~Cliente()
        +int getId()
        +string getNombre()
    }
    
    class Habitacion {
        -int numero
        -string tipo
        -bool ocupada
        +Habitacion(int, string)
        +~Habitacion()
        +int getNumero()
        +string getTipo()
        +bool estaOcupada()
        +void ocupar()
        +void desocupar()
    }
    
    Hotel *-- Habitacion
    Hotel o-- Cliente
```
