```mermaid
classDiagram
  class Habitación{
        -int numero
        -string tipo
        -bool ocupada
        +Habitación(int num, string t)
        +~Habitación()
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
        -vector<Habitación> habitaciones
        -vector<Cliente*> clientes
        +Hotel(string n)
        +~Hotel()
        +void agregarHabitación(int numero, string tipo)
        +void registrarCliente(Cliente* cliente)
        +void mostrarInfo()
    }

    Cliente --o Hotel
    Habitación --* Hotel
  
