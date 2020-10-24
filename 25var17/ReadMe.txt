
using System;
					
public class Program
{
	public static void Main()
	{
		//Поменять местами максимальный и минимальный элемент массива 
		 Random r = new Random();
            int N, i, S;
            N = r.Next(5, 10);
            int[] A = new int[N];
            for (i = 0; i < N; i++)
            {
                A[i] = r.Next(0, 50);
                Console.Write(A[i] + " ");
 
            }
 
            int min;
            int max;
            for (i = 0; i < N; i++)
            {
                Console.WriteLine();
            }
            max = A[0];
            min = A[0];
            for (i = 0; i < N; i++)
            {
                if (A[i] > max)
                {
                    max = A[i];
                }
                if (A[i] < min)
                {
                    min = A[i];
                    S = max; max = min; min = S;
                }
            }
 
            Console.WriteLine("Максимальное число в массиве: {0}", max);
            Console.WriteLine("Минимальное число в массиве: {0}", min);
    }
}
