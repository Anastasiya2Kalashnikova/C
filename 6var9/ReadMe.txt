using System;
					
public class Program
{
	public static void Main()
	{
		//Дано  целое  положительное  число.  Вывести символы,  изображающие  цифры  этого  числа (впорядке справа налево).
		uint x = uint.Parse(Console.ReadLine());
while (x > 0)
{
   Console.Write(x % 10);
   x /= 10;
}

Console.WriteLine(true);
		
		
	}
}
