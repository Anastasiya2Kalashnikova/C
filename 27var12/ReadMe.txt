using System;
					
public class Program
{
	public static void Main()
	{
		//Сожмите массив, выбросив каждый второй его элемент (дополнительные массивы использовать не разрешается
		Console.Write("Размер массива: ");
        int n = int.Parse(Console.ReadLine());
        int[] a = new int[n];
        Random rnd = new Random();
        for (int i = 0; i < n; i++)
        {
            a[i] = rnd.Next(-10, 11);
            Console.Write("" + a[i] + " ");
        }
        Console.WriteLine();
        for (int i = 1; i < a.Length; i++)
        {
            for (int j = i + 1; j < a.Length; j++)
                a[j - 1] = a[j];
            Array.Resize(ref a, a.Length - 1);
        }
        for (int i = 0; i < a.Length; i++)
            Console.Write("" + a[i] + " ");
       // Console.WriteLine();
        Console.WriteLine(true);
	}
}
