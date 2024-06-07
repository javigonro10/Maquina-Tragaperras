# Proyecto de Juego de Tragaperras

¡Bienvenido al proyecto de Juego de Tragaperras! Este proyecto simula un sencillo juego de tragaperras utilizando Python. El juego permite a los jugadores depositar dinero, realizar apuestas en varias líneas, girar la máquina tragaperras y verificar sus ganancias. El proyecto está diseñado para demostrar conceptos básicos de programación en Python, como bucles, funciones y condicionales.

## Características

- **Depositar Dinero**: Los jugadores pueden depositar una cantidad especificada de dinero para empezar a jugar.
- **Realizar Apuestas**: Los jugadores pueden elegir el número de líneas en las que apostar y la cantidad a apostar en cada línea.
- **Girar la Máquina Tragaperras**: La máquina tragaperras generará símbolos aleatorios para cada columna y fila.
- **Verificar Ganancias**: Después de cada giro, el juego verifica las líneas ganadoras y calcula las ganancias en función de los símbolos y la cantidad apostada.
- **Seguir Jugando**: Los jugadores pueden seguir jugando mientras tengan dinero en su saldo o elijan abandonar.

## Instalación

Para ejecutar este proyecto, necesitas tener Python instalado en tu sistema. Puedes descargar Python desde [aquí](https://www.python.org/downloads/).

## Cómo Jugar

1. **Clonar el Repositorio**: Clona este repositorio en tu máquina local utilizando:
    ```bash
    git clone https://github.com/tu-usuario/slot-machine-game.git
    ```

2. **Navegar al Directorio del Proyecto**: 
    ```bash
    cd slot-machine-game
    ```

3. **Ejecutar el Juego**:
    ```bash
    python slot_machine.py
    ```

## Estructura del Proyecto

- `slot_machine.py`: El script principal de Python que contiene toda la lógica del juego.

## Descripción del Código

A continuación, se presenta una breve descripción de los componentes principales del código:

### Constantes y Símbolos

```python
MAX_LINES = 3
MAX_BET = 200
MIN_BET = 1

ROWS = 3
COLS = 3

symbol_count = {
    "A": 2,
    "B": 4,
    "C": 6,
    "D": 8,
}

symbol_value = {
    "A": 5,
    "B": 4,
    "C": 3,
    "D": 2,
}
```

### Funciones

- `check_winnings(columns, lines, bet, values)`: Verifica si hay líneas ganadoras y calcula las ganancias.
- `get_slot_machine_spin(rows, cols, symbols)`: Genera un giro aleatorio para la máquina tragaperras.
- `print_slot_machine(columns, rows_to_print=3)`: Imprime las columnas de la máquina tragaperras en la consola.
- `deposit()`: Solicita al jugador que ingrese una cantidad de depósito.
- `get_number_of_lines()`: Solicita al jugador que ingrese el número de líneas en las que apostar.
- `get_bet()`: Solicita al jugador que ingrese la cantidad a apostar en cada línea.
- `spin(balance)`: Maneja la lógica principal para girar la máquina tragaperras y calcular el saldo.

### Función Principal

```python
def main():
    balance = deposit()
    while True:
        print(f"Saldo actual: ${balance}")
        answer = input("Presiona enter para jugar (q para salir)")
        if answer == "q":
            break
        balance += spin(balance)

    print(f"Te quedaste con ${balance}")

if __name__ == "__main__":
    main()
```

## Contribución

Si deseas contribuir a este proyecto, por favor haz un fork del repositorio y utiliza una rama de características. Las solicitudes de incorporación de cambios son bienvenidas.

## Licencia

Este proyecto es de código abierto y está disponible bajo la [Licencia MIT](LICENSE).

## Agradecimientos

- Gracias a la comunidad de Python por los recursos y tutoriales que ayudaron a crear este proyecto.

---

Disfruta jugando al Juego de Tragaperras y ¡diviértete! Si tienes alguna pregunta o comentario, no dudes en abrir un issue en GitHub.
