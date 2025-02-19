import numpy as np

# Definir la matriz A
A = np.array([[7, 3, -9],
              [8, 5, -12],
              [6, 3, -8]])

# Calcular los valores propios y los vectores propios
eigenvalues, eigenvectors = np.linalg.eig(A)

# Mostrar los valores propios y los vectores propios
print("Valores propios:")
print(eigenvalues)
print("\nVectores propios (columnas de la matriz):")
print(eigenvectors)

# Comprobar si la matriz es diagonalizable
# Una matriz es diagonalizable si tiene 3 vectores propios linealmente independientes
rank = np.linalg.matrix_rank(eigenvectors)
Diagonalizable = rank == 3

print("¿Es diagonalizable?", "Sí" if Diagonalizable else "No")
