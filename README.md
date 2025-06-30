Desarrolle la mayoría de ejercicios en clase. Para cada punto cree un programa individual. Al finalizar suba todo a un repo y subalo al canal reto_08 en slack.
1. De los retos anteriores selecione 3 funciones y escribalas en forma de lambdas.

       # Sumar dos números
       suma = lambda a, b: a + b
       print("Suma de 5 y 3:", suma(5, 3))

       # f(x) = x * x ** (1/3) - 1
       funcion_lambda = lambda x: x * (x ** (1/3)) - 1
       print("f(x) con x=8:", funcion_lambda(8))

       # Potencia simple
       potencia = lambda base, exponente: base ** exponente
       print("2^3 =", potencia(2, 3))

2. De los retos anteriores selecione 3 funciones y escribalas con argumentos no definidos (*args).

       # Sumar cualquier cantidad de números
       def sumar_numeros(*args):
           return sum(args)
       print("Suma de 2, 3 y 4:", sumar_numeros(2, 3, 4))

       # Buscar el mayor de n números
       def maximo(*args):
           return max(args)
       print("Máximo entre 1, 5, 3, 9:", maximo(1, 5, 3, 9))

       # Buscar el menor de n números
       def minimo(*args):
           return min(args)
       print("Mínimo entre 6, 2, 8:", minimo(6, 2, 8))

   3. Escriba una función recursiva para calcular la operación de la potencia.
  
          def potencia_recursiva(base: int, exponente: int) -> int:
      
              if exponente == 0:
                  return 1
             
              return base * potencia_recursiva(base, exponente - 1)

          if __name__ == "__main__":
              base = int(input("Ingrese la base: "))
              exponente = int(input("Ingrese el exponente: "))
              resultado = potencia_recursiva(base, exponente)
              print(f"{base}^{exponente} = {resultado}")

4. Utilice la siguiente plantilla de code para contar el tiempo:
     
           import time
       def fibo_iterativo(n: int) -> int:
           n1, n2 = 0, 1
           for _ in range(n):
               n1, n2 = n2, n1 + n2
            return n1

        def fibo_recursivo(n: int) -> int:
            if n <= 1:
               return n
        return fibo_recursivo(n - 1) + fibo_recursivo(n - 2)

        def medir_tiempo(funcion, n: int) -> float:
            start_time = time.time()
            funcion(n)
            end_time = time.time()
            return end_time - start_time

       if __name__ == "__main__":
           print("n\tIterativo (s)\tRecursivo (s)")
           for n in range(5, 40, 5):  # de 5 a 35
               t_iter = medir_tiempo(fibo_iterativo, n)
               t_recur = medir_tiempo(fibo_recursivo, n)
               print(f"{n}\t{t_iter:.6f}\t{t_recur:.6f}")

   


