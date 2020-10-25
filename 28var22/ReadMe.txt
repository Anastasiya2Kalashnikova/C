
using System;
					
public class Program
{
	public static void Main()
	{
		//Сформируйте  двумерный  массив  NxN  по  сле-дующему правилу:  элементы главной диагона-ли равны 1, ниже главной диагонали -0, а выше  -сумме индексов.
	Console.WriteLine("Введите размер квадратной матрицы");
            int n = Convert.ToInt32(Console.ReadLine()); ;
 
            int[,] a = new int[n, n];
 
            for (int i = 0; i < n; i++)
                for (int j = i; j < n; j++)
                    a[i, j] = i + j;
 
            for (int i = 0; i < n; i++)
                for (int j = i; j <= i; j++)
                    a[i, j] = 1;
 
            for (int i = 0; i < n; i++)
            {
                for (int j = 0; j < n; j++)
                    Console.Write("{0}{1}", a[i, j], "\t");
                Console.WriteLine();
            }
            Console.ReadLine();
	}
}
