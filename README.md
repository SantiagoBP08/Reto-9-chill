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

    def mover_ceros_al_final(lista):
    """
    Mueve todos los ceros al final de la lista, manteniendo el orden del resto.
    """
    no_ceros = []   # Lista para guardar los elementos distintos de cero
    ceros = []      # Lista para guardar los ceros

    for numero in lista:
        if numero == 0:
            ceros.append(0)
        else:
            no_ceros.append(numero)

    # Concatenamos la parte sin ceros + los ceros
    resultado = no_ceros + ceros
    return resultado


    # Ejemplo interactivo
    if __name__ == "__main__":
        n = int(input("Ingrese la cantidad de números del arreglo: "))
        arreglo = []

        for i in range(n):
            num = int(input(f"Ingrese el número {i+1}: "))
            arreglo.append(num)

        print("\nArreglo original:", arreglo)
        nuevo_arreglo = mover_ceros_al_final(arreglo)
        print("Arreglo con ceros al final:", nuevo_arreglo)

## 4. Revisar que son los algoritmos de sorting , entender bubble-sort 

4.1 Los algoritmos de sorting sirven para ordenar listas de datos, como por ejemplo números. La idea es ponerlos de menor a mayor o de mayor a menor, dependiendo de lo que se necesite. Esto es útil porque cuando los datos están ordenados, uno los puede buscar más fácil o comparar entre ellos. También se ven más organizados. Hay varios tipos de algoritmos de sorting, algunos son más rápidos, otros más lentos, y cada uno se usa dependiendo del caso. En mi caso, el que estudiamos fue Bubble Sort, que es uno de los más básicos.

4.2 Bubble Sort es un método para ordenar una lista comparando dos elementos seguidos y cambiándolos de lugar si están en el orden incorrecto. Esto lo hace muchas veces, hasta que todo queda bien ordenado. Le dicen “burbuja” porque los números más grandes van “subiendo” poco a poco hasta el final, como una burbuja en el agua.

Al principio se revisan los primeros dos números. Si el primero es más grande que el segundo, se cambian. Luego se revisa el segundo con el tercero, y así hasta el final de la lista. Esa es una pasada. Luego vuelve a empezar, pero ahora ya el número más grande está al final, así que no se revisa más. Esto se repite hasta que ya no haya que hacer más cambios.
