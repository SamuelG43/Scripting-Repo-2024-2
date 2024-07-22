# Taller # 1 

## 1. Realizar cinco programas y responda dos preguntas de teoría, se debe usar C# como lenguaje de Programación, click en el enlace para realizar la autoasignación de los enunciados  [Ejercicios](https://docs.google.com/document/d/1yT7-HVfscZ_biObi1HarsSORy2PruXnnH0Xnzbzr9IE/edit?usp=sharing)

--------------------------------------------------------------------

-   ### 2 sobre uso de funciones
	- **Realice una función que invierta un array de números enteros**
		-	R// 
```c#
		using System;

  

namespace Pruebas_de_Escritorio

{

class Program

{

static void Main(string[] args)

{

int[] Arreglo = new int[3];

Arreglo[0] = 1;

Arreglo[1] = 2;

Arreglo[2] = 3;

  

InvertirArray(Arreglo);

  
  
  

for (int num = 0; num < Arreglo.Length; num++)

{

Console.WriteLine(Arreglo[num]);
}
}
public static void InvertirArray(int[] Arreglo)

{

int i = 0;

int k = 2;

  

while (i < k)

{

int temp = Arreglo[i];

Arreglo[i] = Arreglo[k];

Arreglo[k] = temp;

k--;

i++;
}
}
}

}
```

 

 
-  ***Realizar una función que calcule si una cadena es palíndroma.***	
	- R//
```c#
using System;

using System.Diagnostics;

using System.Security.Cryptography.X509Certificates;

  

namespace Pruebas_de_Escritorio

{

class Program

{

static void Main(string[] args)

{

string Palabra = "rayar";

  

char[] arregloPalabra = Palabra.ToCharArray();

  

VerificarPalindromo(arregloPalabra);

}

  

static void VerificarPalindromo(char[] arregloPalabra)

{

  
  

char[] arregloPalabraInvertida = new char[arregloPalabra.Length];

  

int posicion = 0;

for (int i = arregloPalabra.Length - 1; i >= 0; i--)

{

arregloPalabraInvertida[posicion] = arregloPalabra[i];

posicion++;

}

  
  

string palabraOriginal = new string(arregloPalabra);

string palabraInvertida = new string(arregloPalabraInvertida);

  

if (palabraOriginal == palabraInvertida)

{

Console.WriteLine("Es Palindromo");

}

else

{

Console.WriteLine("No Es Palindromo");

}

}

}
}
```
	
-   ### 1 sobre arreglos o matrices
	- ***Lea correctamente un array de n posiciones, luego llene las posiciones pares con 1 y las posiciones impares con cero.***
		- **R//**		
 ```C#
 using System;

  

namespace Pruebas_de_Escritorio

{

class Program

{

static void Main(string[] args)

{

// Leer el tamaño del array

Console.Write("Ingrese el tamaño del array: ");

int n = int.Parse(Console.ReadLine());

  

// Crear el array con el tamaño especificado

int[] arreglo = new int[n];

  

// Llenar el array con 1s en posiciones pares y 0s en posiciones impares

for (int i = 0; i < arreglo.Length; i++)

{

arreglo[i] = (i % 2 == 0) ? 1 : 0;

}

  

// Mostrar el contenido del array

Console.WriteLine("Contenido del array:");

for (int i = 0; i < arreglo.Length; i++)

{

Console.WriteLine($"Índice {i}: {arreglo[i]}");

}

}

}

}
```
-   ### 1 sobre cadenas
	- ***Lea una cadena de números enteros positivos y luego cree un array con los números de la cadena, se debe validar que la cadena contenga números.***
		- **R//**
```c#
using System;
using System.Linq;

class Program
{
    static void Main()
    {
        Console.WriteLine("Ingrese una cadena de números enteros positivos separados por espacios:");
        string input = Console.ReadLine();

        // Validar que la cadena contenga solo números y espacios
        if (ValidarCadena(input))
        {
            // Crear un array con los números de la cadena
            int[] numeros = ConvertirACadenaDeNumeros(input);
            Console.WriteLine("El array de números es:");
            foreach (int numero in numeros)
            {
                Console.WriteLine(numero);
            }
        }
        else
        {
            Console.WriteLine("La cadena contiene caracteres no válidos. Por favor, ingrese solo números enteros positivos separados por espacios.");
        }
    }

    static bool ValidarCadena(string input)
    {
        return input.All(c => char.IsDigit(c) || c == ' ');
    }

    static int[] ConvertirACadenaDeNumeros(string input)
    {
        // Separar la cadena en partes y convertir cada parte a un número entero
        return input.Split(new[] { ' ' }, StringSplitOptions.RemoveEmptyEntries)
                    .Select(int.Parse)
                    .ToArray();
    }
}
```
- ### 1 sobre condiciones o ciclos
	- R//
```C#
using System;

using System.Diagnostics;

using System.Security.Cryptography.X509Certificates;

  

namespace Pruebas_de_Escritorio

{

class Program

{

static void Main(string[] args)

{

bool condicion = true;

int NumerosIngresados = 0;

float SumaNumeros = 0;

float promedioFinal = 0;

while (condicion == true)

{

Console.Write("Ingresa un numero flotante o ingresa F para finalizar ");

string ValorIngresado = Console.ReadLine();

if (ValorIngresado == "F")

{

condicion = false;

}

else

{

if (float.TryParse(ValorIngresado, out float numero))

{

NumerosIngresados++;
SumaNumeros += numero;
}
}
}
promedioFinal = SumaNumeros / NumerosIngresados;
Console.WriteLine(promedioFinal);
}
}
}
```
    



- ### 2 preguntas de teoría
	- 	- **Inicialice y declare 5 variables de diferente tipo.**
		-   ***R//*** public int Edad;

			public float Vida;

			public char VariableChar;

			private string Nombre;

			public double VariableDouble;
	- **¿Cuál es la salida del siguiente código?**
	
		![](https://lh7-us.googleusercontent.com/docsz/AD_4nXeAGxA5eyYm-TMilm7maH3Lglt8XKoCLCwvYynC2ZN9LVs35bGbENwd_LvlAzki-BAml6NjoXlkaS_LgXeb2D9apE7cev08gwlvRKCVw5dR9RTc5rzRYe01uCrFwGyjoUYyTWLfxsg3CT39BFweUfEV-Rz-?key=RS0dGF4dmDM60FnuwYR2xA)
		-	***R//*** El bucle  `do-while`  se vuelve infinito porque en cada ciclo se le da a la variable  `i`  el valor 10 antes de verificar si  `--i > 0`. Esto significa que  `i`  siempre empieza en 10 y luego se reduce a 9 antes de evaluar la condición, lo que hace que la condición siempre sea verdadera.
Como resultado, el programa queda atrapado en el bucle y nunca llega a la línea  `Console.WriteLine(i)`.
Para resolverlo hay que hacer lo siguiente en la línea de código:
```C#
int i = 10; // Mover esta línea fuera del bucle
do
{
    // Resto del código
} while (--i > 0);
Console.WriteLine(i);
}
```

