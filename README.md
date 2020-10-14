# Taller1

{
    class Program
    {
        static void Main(string[] args)
        {
            
            //Se crea la variable ejercicios para que se pueda escoger el que se desee ejecutar.
            int Ejercicios = 1;

            //Se crea ciclo while para que no se cierre el programa despues de que se ejecute un ejercicio y solo se podra salir ingresando el numero 8.
            while (Ejercicios != 0)
            {
                Console.WriteLine("                     Bienvenido a los ejercicios del aprendiz, \n" +
                                  "                         Cristian Camilo Espitia Guerrero \n" +
                                  "                         Adsi Ficha 2067791\n" +
                                  "                         Instructor\n" +
                                  "                         Jesus Ropero Barbosa\n" +
                                  "                  Por favor seleccione el ejercicio que desea ver\n" +
                                  "");

                Console.WriteLine("Ejercicio 1 ");
                Console.WriteLine("Ejercicio 2 ");
                Console.WriteLine("Ejercicio 3 ");
                Console.WriteLine("Ejercicio 4 ");
                Console.WriteLine("Ejercicio 5 ");
                Console.WriteLine("Ejercicio 6 ");
                Console.WriteLine("Ejercicio 7 ");
                Console.WriteLine("Ejercicio 8 ");
                Console.WriteLine("Marque 9 para salir");
                Ejercicios = Convert.ToInt32(Console.ReadLine());
                Console.Clear();

                switch (Ejercicios)
                {
                    case 1:
                         // Ejercicio I 
                         //Se define la variable numero a ingresar para guardar allí el numero que ingrese el usuario. 
                        int NumeroIngresado = 0;

                        Console.WriteLine("Bienvedido al primer ejercicio en C# consola\n" +
                            "");
                        Console.WriteLine("Ingrese por favor un número");
                        NumeroIngresado = int.Parse(Console.ReadLine());


                        if (NumeroIngresado % 2 == 0)
                        {
                            Console.WriteLine("El número " + NumeroIngresado + " es par");
                        }
                        else
                        {
                            Console.WriteLine("El número " + NumeroIngresado + " es impar");
                        }
                        Console.ReadKey();
                        break;
                    case 2:

                        // Ejercicio II

                        // Se declara la variable NumeroTabla para guardar allí el numero que ingrese el usuario.
                        int NumeroTabla = 0;
                        // Se declara variable resultado para guardar el la multiplicación del numero ingresado por el usuario y i.
                        int Resultado = 0;
                        Console.WriteLine("Bienvedido al segundo ejercicio en C# consola\n" +
                            "");
                        Console.WriteLine("Ingrese por favor un número del cual desea saber la tabla de multiplicar\n" +
                            "");
                        NumeroTabla = int.Parse(Console.ReadLine());
                        Console.WriteLine("La tabla de multiplicar que desea ver es del numero\n" +
                            "" + NumeroTabla);

                        //Se declara un for para que el numero ingresado por el usuario se multiplique 10 veces por i
                        Console.WriteLine("La tabla de multiplicar del número " + NumeroTabla + " Es ");
                        for (int i = 1; i < 11; i++)
                        {
                            Resultado = NumeroTabla * i;
                            Console.WriteLine(NumeroTabla + "X" + i + " = " + Resultado);
                        }
                        Console.ReadKey();
                        break;
                    case 3:

                        // Ejercicio III
                        int[] tablas = new int[9];
                        Console.WriteLine("Bienvedido al tercer ejercicio en C# consola\n" +
                            "");
                        Console.WriteLine("Se mostraran las tablas de multiplicar del 2 al 9 cada una hasta el 10\n" +
                            "");
                        for (tablas[0] = 2; tablas[0] <= 9; tablas[0]++)
                        {
                            Console.WriteLine("Tabla de multiplicar del {0}", tablas[0]);
                            Console.WriteLine("--------------------------------");
                            for (int i = 1; i <= 10; i++)
                            {
                                Console.WriteLine("{0} * {1} = {2}", tablas[0], i, (tablas[0] * i));
                            }
                        }
                        Console.ReadKey();
                        break;
                    case 4:

                        // Ejercicio IV

                        Console.WriteLine("Bienvedido al cuarto ejercicio en C# consola\n" +
                            "");


                        int NumeroPrimo;
                        int control = 0;
                        int division;
                        Console.WriteLine("Digite por favor un numero que sea mayor a 1\n" +
                            "");
                        NumeroPrimo = int.Parse(Console.ReadLine());
                        for (int d = 2; d < NumeroPrimo; d++)
                        {
                            division = NumeroPrimo % d;
                            if (division == 0)
                            {
                                control = control + 1;
                            }
                        }
                        if (control >= 1)
                        {
                            Console.WriteLine("El numero no es primo: " + NumeroPrimo);
                        }
                        else
                        {
                            Console.WriteLine("El numero es primo: " + NumeroPrimo);
                        }

                        Console.ReadKey();
                        break;
                    case 5:

                        // Ejercicio V

                        Console.WriteLine("Bienvedido al quinto ejercicio en C# consola\n" +
                            "");

                        Console.WriteLine("Las edades registradas son 12, 50, 23, 10, 18, 35, 41, 85, 16, 45 y el orden asendente de las edades son\n" +
                            "");
                        int[] edades = { 12, 50, 23, 10, 18, 35, 41, 85, 16, 45 };

                        Array.Sort(edades);

                        for (int i = 0; i < edades.Length; i++)
                        {
                            Console.WriteLine(edades[i].ToString());
                        }
                        Console.ReadKey();
                        break;
                    case 6:

                        // Ejercicio VI

                        Console.WriteLine("Bienvedido al sexto ejercicio en C# consola\n" +
                            "");

                        Console.WriteLine("Buscar Usuario y mostrar su edad\n" +
                            "");

                        int[] edad = { 12, 50, 23, 10, 18, 35, 41, 85, 16, 45 };
                        string[] nombres = { "juan", "maria", "teresa", "pedro", "javier", "ana", "diana", "jorge", "dayana", "lady" };
                        string NombreBuscar;

                        /* definir dos variables */
                        Boolean existe = false; /* me a decir si el ususario exisete */
                        int indice = 0;  /* guardare el valor de la posicion del arreglo  donde existe el usasrio */

                        int indiceMayor = 0;
                        int edadMayor = 0;

                        Console.WriteLine(" - muestra el array de nombre");

                        foreach (string nombre in nombres)
                        {
                            Console.Write(nombre + " - ");
                        }

                        Console.Write("\n");

                        Console.Write("Digite el nombre del usuario que desea buscar: \n" +
                            "");
                        NombreBuscar = Console.ReadLine();

                        for (int i = 0; i < nombres.Length; i++)
                        {

                            // Se busco el nombre
                            if (NombreBuscar == nombres[i])
                            {
                                existe = true;
                                indice = i;
                            }
                            // Se comparo las edades 
                            if (edad[i] > edadMayor)
                            {
                                edadMayor = edad[i];
                                indiceMayor = i;
                            }
                        }
                        if (existe)
                        {
                            Console.WriteLine(" El usuario " + NombreBuscar + " tiene " + edad[indice] + " años");
                        }
                        else
                        {
                            Console.WriteLine(" El usuario " + NombreBuscar + " no exiiste ");
                        }
                        Console.ReadKey();
                        break;
                    case 7:

                        // Ejercicio VII

                        Console.WriteLine("Bienvedido al séptimo ejercicio en C# consola\n" +
                            "");

                        Console.WriteLine("Se buscaran lo el usuario de más edad y el de menor edad en el sistema\n" +
                            "");

                        int[] edad2 = { 12, 50, 23, 10, 18, 35, 41, 85, 16, 45 };
                        string[] nombres2 = { "juan", "maria", "teresa", "pedro", "javier", "ana", "diana", "jorge", "dayana", "lady" };
                        int indiceMayor2 = 0;
                        int edadMayor2 = 0;
                        int indiceMenor = 0;
                        int MenorEdad = 0;

                        for (int i = 0; i < nombres2.Length; i++)
                        { 
                            if (edad2[i] > edadMayor2)
                            {
                                edadMayor2 = edad2[i];
                                indiceMayor2 = i;

                                if (edad2[i] < MenorEdad)
                                {
                                    MenorEdad = edad2[i];
                                    indiceMenor = i;
                                }
                            }
                        }
                        for (int i = 0; i < edad2.Length; i++)
                            for (int j = 0; j < edad2.Length; j++)
                            {
                                if (edad2[i] > edadMayor2)
                                {
                                    edadMayor2 = edad2[i];
                                    indiceMayor2 = i;

                                }
                                if (edad2[j] > edadMayor2)
                                {
                                    MenorEdad = edad2[j];
                                    indiceMenor = j;
                                }
                            }
                        Console.WriteLine("El usuario Mayor es " + nombres2[indiceMayor2] + " y su edad es  " + edad2[indiceMayor2] + " años\n" +
                            "");
                        Console.WriteLine("Y el usuario menor es " + nombres2[indiceMenor] + " y su edad es  " + edad2[indiceMenor] + " años");
                        Console.ReadKey();
                        break;

                    // Ejercicio VIII

                    case 8:
                        
                        string Palabra, PalabraInversa, Caracter;

                        Console.WriteLine("Ingrese por favor una palabra");
                        Palabra = Convert.ToString(Console.ReadLine());
                        int p;
                        p = Palabra.Length;
                        PalabraInversa = "";
                        for (int a = p - 1; a >= 0; a--)
                        {
                            Caracter = Palabra.Substring(a, 1);
                            PalabraInversa = PalabraInversa + Caracter;
                        }
                        if (Palabra == PalabraInversa)
                        {
                            Console.WriteLine("La palabra "+ Palabra+ " es palindrome");
                            Console.WriteLine(PalabraInversa);
                        }
                        else
                        {
                            Console.WriteLine("La palabra "+ Palabra +" no es palindrome");
                            Console.WriteLine(PalabraInversa);
                        }
                        Console.ReadKey();
                        break;
                }
            }
            Console.ReadKey();
        }
    }
}
