# RETO #9
Desarrolle la mayoría de los ejercicios en clase. Para cada punto cree un programa individual. Al finalizar suba todo a un repo y subalo al canal reto_10 en slack.

## 1. Desarrollar un algoritmo que calcula el promedio de un arreglo de reales.

    def calcular_promedio(lista_reales):
        """
        Calcula el promedio de los elementos de una lista de números reales.
    
        Parámetro:
        - lista_reales: Lista de números reales (floats)

        Retorna:
        - El promedio (float)
        """
        if len(lista_reales) == 0:
            return 0  # Evita división por cero
        suma = sum(lista_reales)
        promedio = suma / len(lista_reales)
        return promedio

    # Ejemplo de uso
    if __name__ == "__main__":
        datos = [3.5, 4.2, 5.0, 2.8, 6.1]
        print(f"El promedio del arreglo es: {calcular_promedio(datos)}")

## 2. Desarrollar un algoritmo que calcula el producto punto de dos arreglos de números enteros (reales) de igual tamaño.

    def producto_punto(v1, v2):
    """
    Calcula el producto punto entre dos listas del mismo tamaño.
    """
    if len(v1) != len(v2):
        print("Error: Los vectores deben tener el mismo tamaño.")
        return None

    resultado = 0
    for i in range(len(v1)):
        resultado += v1[i] * v2[i]
    return resultado


    # Ejemplo interactivo (con input del usuario)
    if __name__ == "__main__":
        n = int(input("Ingrese la cantidad de elementos de los vectores: "))

        vector1 = []
        vector2 = []

        print("\nIngrese los elementos del primer vector:")
        for i in range(n):
            num = float(input(f"Elemento {i+1}: "))
            vector1.append(num)

        print("\nIngrese los elementos del segundo vector:")
        for i in range(n):
            num = float(input(f"Elemento {i+1}: "))
            vector2.append(num)

        resultado = producto_punto(vector1, vector2)
        print(f"\nEl producto punto de los vectores es: {resultado}")

## 3. Hacer un algoritmo que deja al final de un arreglo de números todos los ceros que aparecen en dicho arreglo.
