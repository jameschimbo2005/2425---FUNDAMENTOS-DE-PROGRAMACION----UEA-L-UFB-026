# Matriz bidimensional 3x3
matriz = [
    [10, 25, 30],
    [45, 50, 60],
    [70, 85, 90]
]

# Función para ordenar una fila específica usando Bubble Sort
def ordenar_fila(matriz, fila):
    n = len(matriz[fila])
    for i in range(n):
        for j in range(0, n - i - 1):
            if matriz[fila][j] > matriz[fila][j + 1]:
                matriz[fila][j], matriz[fila][j + 1] = matriz[fila][j + 1], matriz[fila][j]

# Mostrar matriz original
print("Matriz original:")
for fila in matriz:
    print(fila)

# Selección de fila a ordenar
fila_a_ordenar = int(input("Ingresa el número de la fila que deseas ordenar (0, 1 o 2): "))

# Ordenar la fila elegida
if 0 <= fila_a_ordenar < len(matriz):
    ordenar_fila(matriz, fila_a_ordenar)
    print("\nMatriz con la fila ordenada:")
    for fila in matriz:
        print(fila)
else:
    print("Número de fila inválido.")
