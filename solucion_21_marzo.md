```mermaid
classDiagram
  class Habitacion{
        -int numero
        -string tipo
        -bool ocupada
        +Habitacion(int num, string t)
        +~Habitacion()
        +int getNumero() 
        +string getTipo() 
        +bool estaOcupada() 
        +void ocupar() 
        +void desocupar()
    }
    class Cliente{
        -int id
        -string nombre
        +Cliente(int i, string n)
        +~Cliente()
        +int getId()
    }
    class Hotel{
        -string nombre;
        -vector<Habitacion> habitaciones
        -vector<Cliente*> clientes
        +Hotel(string n)
        +~Hotel()
        +void agregarHabitacion(int numero, string tipo)
        +void registrarCliente(Cliente* cliente)
        +void mostrarInfo()
    }

    Cliente --o Hotel
    Habitacion --* Hotel
  
