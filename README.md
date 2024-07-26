# Taller # 1 

## 1. Realizar cinco programas y responda dos preguntas de teoría, se debe usar C# como lenguaje de Programación, click en el enlace para realizar la autoasignación de los enunciados  [Ejercicios](https://docs.google.com/document/d/1yT7-HVfscZ_biObi1HarsSORy2PruXnnH0Xnzbzr9IE/edit?usp=sharing)

--------------------------------------------------------------------

### 2 sobre uso de funciones
**Realice una función que invierta un array de números enteros**

```
using System;

namespace Pruebas_de_Escritorio
{
    class Program
    {
        static void Main(string[] args)
        {
            int[] Arreglo = new int[] { 1, 2, 3, 4, 5 };

            
            Console.WriteLine("arreglo\n");
            for (int num = 0; num < Arreglo.Length; num++)
            {
                
                Console.WriteLine(Arreglo[num] + "\n");
            }
            
            Console.WriteLine("\n");
            InvertirArray(Arreglo);
        }

        public static void InvertirArray(int[] Arreglo)
        {
            int i = 0;
            int k = Arreglo.Length - 1;

            while (i < k)
            {
                int temp = Arreglo[i];
                Arreglo[i] = Arreglo[k];
                Arreglo[k] = temp;
                k--;
                i++;
            }
            Console.WriteLine("arreglo inverso:\n");
            for (int num = 0; num < Arreglo.Length; num++)
            {

                Console.WriteLine(Arreglo[num] + "\n");
            }
        }
    }
}

```

 

 
**Realizar una función que calcule si una cadena es palíndroma.**	

```
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
	
### 1 sobre arreglos o matrices

**Lea correctamente un array de n posiciones, luego llene las posiciones pares con 1 y las posiciones impares con cero.**
				
 ```
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
                if (i % 2 == 0)
                {
                    arreglo[i] = 1;
                }
                else if (i % 2 != 0)
                {
                    arreglo[i] = 0;
                }

                
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
### 1 sobre cadenas
**Lea una cadena de números enteros positivos y luego cree un array con los números de la cadena, se debe validar que la cadena contenga números.**
		- 
```
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
### 1 sobre condiciones o ciclos
**Usando un ciclo while, ingrese n valores flotantes, cada que ingrese un número acumúlelo en una variable, al final calcule el promedio de los números ingresados.**
	
```
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
                Console.Write("Ingresa un numero flotante o ingresa F para finalizar: ");
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
    



### 2 preguntas de teoría
**Inicialice y declare 5 variables de diferente tipo.**
```
     public int Edad = 5;
     public float Vida = 5.0f;
     public char VariableChar ='A';
     private string Nombre = “gustavo”;     
     private bool EsVerdadero = true;;

```

**¿Qué es un ciclo infinito? Escriba un ejemplo**
```
public int numero =  5;

while ( numero == 5)
{
Console.WriteLine("Hola");
}

```
# 20 firmas de funciones

### *CON PARAMETRO Y RETORNO*

- ### Suma:  
  
```
	int resultado = sumar(1, 2);
	
	  
	
	static int sumar(int numero1, int numero2) //FIRMA
	
	{
	
		return numero1 + numero2;
	
	}
```
    

- **Resta:**  
  
```c#  
	int resultado = restar(1, 2);
	
	static int restar(int numero1, int numero2)//FIRMA
	{
	
		return numero1 - numero2;
	}
```  

 **Multiplicación:**  
  
  ```  
	int resultado = multiplicar(1, 2);
	
	static int multiplicar(int numero1, int numero2)//FIRMA
	
	{
	
		return numero1 * numero2;
	
	}
```
    
  **División:**  
  ```	
	int resultado = dividir(1, 2);

	static int dividir(int numero1, int numero2)//FIRMA

	{

		return numero1 / numero2;

	}
```
 
 **Concatenación:**  
  
  ```c#
	string resultado = Concatenar("Hola", " Mundo");

	public string Concatenar(string str1, string str2)//FIRMA

	{

		return str1 + str2;

	}
```    
    

### ***SIN PARÁMETRO Y CON RETORNO***
```

 
  
  
	int resultado = sumar();
	
	  
	
	static int sumar()//FIRMA
	
	{
	
		int numero1 = 1; // Define valores por defecto
	
		int numero2 = 2;
	
	r	eturn numero1 + numero2;

	}
```
   
**Resta:**  
  
  ```
	int resultado = restar();
	
	static int restar()//FIRMA
	
	{
	
		int numero1 = 5; // Define valores por defecto
	
		int numero2 = 3;
	
		return numero1 - numero2;
	
	}
```  
    

**Multiplicación:**  
  ```
	int resultado = multiplicar();
	
	static int multiplicar()//FIRMA
	
	{
	
		int numero1 = 4; // Define valores por defecto
		
		int numero2 = 3;
	
		return numero1 * numero2;
	
	}
```   
    
**División:**  
  ```
	  
	int resultado = dividir();
	
	static int dividir()//FIRMA
	
	{
	
		int numero1 = 10; // Define valores por defecto
	
		int numero2 = 2;
	
		return numero1 / numero2;
	
	}
```
   
    

**Concatenación:**  
```
   
	string resultado = Concatenar();
	
	public string Concatenar()//FIRMA
	
	{
	
		return "Hola" + " Mundo";
	
	}
```
  
    

**Obtener Fecha Actual:**  
```
  
	DateTime fecha = ObtenerFechaActual();
	
	public DateTime ObtenerFechaActual()//FIRMA
	
	{
	
		return DateTime.Now;
	
	}
```
**Generar Número Aleatorio:**  
  
  ```
	int numeroAleatorio = GenerarNumeroAleatorio();
	
	public int GenerarNumeroAleatorio()//FIRMA
	
	{
	
		Random rand = new Random();
	
	return rand.Next();
	
	}

```
**Leer Cadena:**  
  ```
	string entrada = LeerCadena();
	
	public string LeerCadena()//FIRMA
	
	{
	
		return Console.ReadLine();
	
	}
```
  
    

### CON PARAMETRO Y SIN RETORNO

**Imprimir Mensaje:** 
  
  ```
	ImprimirMensaje("Hola Mundo");
	
	public void ImprimirMensaje(string mensaje)//FIRMA
	
	{
	
		Console.WriteLine(mensaje);
	
	}
```
   
    
**Restar:**  
  ```
	int numero1 = 10; // Definir valores de ejemplo
	
	int numero2 = 5;
	
	restar(numero1, numero2);
	
	public void restar(int numero1, int numero2)//FIRMA
	
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
	
	public void sumar(int numero1, int numero2)//FIRMA
	
	{
	
		int resultado = numero1 + numero2;
	
	C	onsole.WriteLine(resultado);
	
	}
 ``` 

### SIN PARAMETRO Y SIN RETORNO

*Imprimir Mensaje:*  
  
  ```c#
	ImprimirMensaje();

	public void ImprimirMensaje()//FIRMA

	{

		Console.WriteLine("Hola");

	}
``` 
   
**Limpiar Pantalla:**  
  
  ```c#
	LimpiarPantalla();

	public void LimpiarPantalla()//FIRMA

	{

		Console.Clear();

	}
```
   

### *USO DE CLASES*

**Crear Persona:**  
  ```c#
  
	Persona pedrito = CrearPersona("Juan", 30);

	public Persona CrearPersona(string nombre, int edad)//FIRMA

	{

		return new Persona { Nombre = nombre, Edad = edad };

	}
``` 
    

**Actualizar Edad:**  
  
  ```c#
	Persona pepito = new Persona { Nombre = "Pepito", Edad = 30 };

	ActualizarEdad(pepito, 35);


	public void ActualizarEdad(Persona persona, int nuevaEdad)//FIRMA

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
		
		
		
		Console.WriteLine("La suma de " + numero1 + " y " + numero2 + " es: " + suma);
	
	}
	
	static int ________(int ________ , int ________)

	{
	
	// Implementar la función para sumar dos números
	
	}

}

```

