# Taller # 1 

## 1. Realizar cinco programas y responda dos preguntas de teoría, se debe usar C# como lenguaje de Programación, click en el enlace para realizar la autoasignación de los enunciados  [Ejercicios](https://docs.google.com/document/d/1yT7-HVfscZ_biObi1HarsSORy2PruXnnH0Xnzbzr9IE/edit?usp=sharing)

--------------------------------------------------------------------

-   ### 2 sobre uso de funciones

-   ### 1 sobre arreglos o matrices
    
-   ### 1 sobre cadenas
    
-   ###  1 sobre condiciones o ciclos
	-  **Usando un ciclo do-while calcule la suma de los primeros n números impares.**
``` c#
class Program
{
    static void Main()
    {
        Console.Write("Ingrese un número (n): ");
        int n = int.Parse(Console.ReadLine());

        int suma = 0;
        int numero = 1; // Comenzamos con el primer número impar

        do
        {
            suma += numero;
            numero += 2; // Avanzamos al siguiente número impar
        } while (numero <= 2 * n); // Continuamos hasta que alcancemos el doble de n

        Console.WriteLine($"La suma de los primeros {n} números impares es: {suma}");
    }
}
```

- ### 2 preguntas de teoría
	- **¿Cuál es la salida del siguiente código?**
	
		![](https://lh7-us.googleusercontent.com/docsz/AD_4nXeAGxA5eyYm-TMilm7maH3Lglt8XKoCLCwvYynC2ZN9LVs35bGbENwd_LvlAzki-BAml6NjoXlkaS_LgXeb2D9apE7cev08gwlvRKCVw5dR9RTc5rzRYe01uCrFwGyjoUYyTWLfxsg3CT39BFweUfEV-Rz-?key=RS0dGF4dmDM60FnuwYR2xA)
		-	***R//*** La salida de este programa va a ser un número de valor menor a 10 hasta el 1 para cumplir con la condición. El resultado sería 9,8,7,6,5,4,3,2,1.
	
	- **Inicialice y declare 5 variables de diferente tipo.**
		-   ***R//*** public int Edad;

			public float Vida;

			public char VariableChar;

			private string Nombre;

			public double VariableDouble;
    

	
