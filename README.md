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


## 20 firmas de funciones

### *CON PARAMETRO Y RETORNO*

- ### Suma:  
  
```c#
int resultado = sumar(1, 2);

  

static int sumar(int numero1, int numero2)

{

return numero1 + numero2;

}
```
    

- **Resta:**  
  
```c#  
int resultado = restar(1, 2);

static int restar(int numero1, int numero2)
{

return numero1 - numero2;
}
```  

 **Multiplicación:**  
  
  ```  c#
int resultado = multiplicar(1, 2);

static int multiplicar(int numero1, int numero2)

{

return numero1 * numero2;

}
```
    
  **División:**  
  ```c#
int resultado = dividir(1, 2);

static int dividir(int numero1, int numero2)

{

return numero1 / numero2;

}
```
 
 **Concatenación:**  
  
  ```c#
string resultado = Concatenar("Hola", " Mundo");

public string Concatenar(string str1, string str2)

{

return str1 + str2;

}
```    
    

### ***SIN PARÁMETRO Y CON RETORNO***
```c#

Suma:  
  
  
int resultado = sumar();

  

static int sumar()

{

int numero1 = 1; // Define valores por defecto

int numero2 = 2;

return numero1 + numero2;

}
```
   
**Resta:**  
  
  ```c#
int resultado = restar();

static int restar()

{

int numero1 = 5; // Define valores por defecto

int numero2 = 3;

return numero1 - numero2;

}
```  
    

**Multiplicación:**  
  ```c#
int resultado = multiplicar();

static int multiplicar()

{

int numero1 = 4; // Define valores por defecto

int numero2 = 3;

return numero1 * numero2;

}
```   
    
**División:**  
  ```c#
  
int resultado = dividir();

static int dividir()

{

int numero1 = 10; // Define valores por defecto

int numero2 = 2;

return numero1 / numero2;

}
```
   
    

**Concatenación:**  
```c#
   
string resultado = Concatenar();

public string Concatenar()

{

return "Hola" + " Mundo";

}
```
  
    

**Obtener Fecha Actual:**  
```c#
  
DateTime fecha = ObtenerFechaActual();

public DateTime ObtenerFechaActual()

{

return DateTime.Now;

}
```
**Generar Número Aleatorio:**  
  
  ```c#
int numeroAleatorio = GenerarNumeroAleatorio();

public int GenerarNumeroAleatorio()

{

Random rand = new Random();

return rand.Next();

}  
    
**Leer Cadena:**  
  ```c#
string entrada = LeerCadena();

public string LeerCadena()

{

return Console.ReadLine();

}
```
  
    

### CON PARAMETRO Y SIN RETORNO

**Imprimir Mensaje:** 
  
  ```c#
ImprimirMensaje("Hola Mundo");

public void ImprimirMensaje(string mensaje)

{

Console.WriteLine(mensaje);

}
```
   
    
**Restar:**  
  ```c#
int numero1 = 10; // Definir valores de ejemplo

int numero2 = 5;

restar(numero1, numero2);

public void restar(int numero1, int numero2)

{

int resultado = numero1 - numero2;

Console.WriteLine(resultado);

}
```


**Sumar:**  
  ```c#
  
int numero1 = 5; // Definir valores de ejemplo

int numero2 = 3;

sumar(numero1, numero2);

public void sumar(int numero1, int numero2)

{

int resultado = numero1 + numero2;

Console.WriteLine(resultado);

}
 ``` 

### SIN PARAMETRO Y SIN RETORNO

*Imprimir Mensaje:*  
  
  ```c#
ImprimirMensaje();

public void ImprimirMensaje()

{

Console.WriteLine("Hola");

}
``` 
   
**Limpiar Pantalla:**  
  
  ```c#
LimpiarPantalla();

public void LimpiarPantalla()

{

Console.Clear();

}
```
   

### *USO DE CLASES*

**Crear Persona:**  
  ```c#
  
Persona pedrito = CrearPersona("Juan", 30);

public Persona CrearPersona(string nombre, int edad)

{

return new Persona { Nombre = nombre, Edad = edad };

}
``` 
    

**Actualizar Edad:**  
  
  ```c#
Persona pepito = new Persona { Nombre = "Pepito", Edad = 30 };

ActualizarEdad(pepito, 35);


public void ActualizarEdad(Persona persona, int nuevaEdad)

{

persona.Edad = nuevaEdad;

}
```
##  Actividad para demostrar funciones a compañeros

  
```c#
using System;

class Program

{

static void Main()

{

int numero1 = 8;

int numero2 = 12;

int suma = ________(________, ________); // Completar la función para sumar dos números

i

Console.WriteLine("La suma de " + numero1 + " y " + numero2 + " es: " + suma);

}

static int ________(int ________ , int ________)

{

// Implementar la función para sumar dos números

}

}

```

