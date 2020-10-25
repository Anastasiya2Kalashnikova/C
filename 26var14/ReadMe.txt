
using System;
		using System.Collections.Generic;
		using System.Linq;
		using System.Text;
					
public class Program
{
	public static void Main()
	{
		//Найти сумму максимальных элементов каждой строки массива
		
		
            double[,] a = new double[3, 4];
 
            Random r = new Random();
            for(int i =0;i<3;i++)
                for (int j = 0; j < 4; j++)
                {
                    a[i, j] = r.NextDouble();
                }
 
            double currMax = 0;
            double sum = 0;
 
            for (int i = 0; i < 3; i++)
            {
                for (int j = 0; j < 4; j++)
                {
                    Console.Write(String.Format("{0:f}  ", a[i, j]));
                }
                Console.WriteLine();
            }
 
 
            for (int i = 0; i < 3; i++)
            {
                currMax = a[i, 0];
                for (int j = 0; j < 4; j++)
                {
                    if (a[i, j] > currMax) currMax = a[i, j];                    
                }
                sum += currMax;                
            }
            Console.WriteLine("{0:f}",sum);
           
		
		
		
	/*	
		
		int[] a, b, c;
		a = new int[5];
		b = new int[6];
		c = new int[4];
		Random rnd = new Random();//Заполняеммассив а случайными числами
		for    (int    i    =    0;    i    < a.GetLength(0); i++)
		a[i] = rnd.Next(1, 100);//Заполняем массив b случайными числами
		for(int i=    0; i< b.GetLength(0); i++)
			b[i] = rnd.Next(1, 100);//Рассчитываеммассивс
		for (int i = 0; i < c.GetLength(0); i++)
			c[i] = a[i] + b[i];//объявление массива с явной инициализацией
		int[] x = {5, 5, 6, 6, 7, 7};//объявление  массивов  с  отложенной  инициали-зацией
		int[] u, v1,v2;
		u = new int[3];
		for (int i = 0; i < 3; i++) 
			u[i] = i + 1;//v1={1,2,3};недопустимое присваивание
		v1 = new int[4];
		v1 = u; //допустимое присваивание
		v2 = new int[4];
		for (int i = 0; i < 3; i++) 
			v2[i] = u[i]*2;// Создадим Класс Arr с методом PrintArr для вы-вода массивов на печать
	
		Arr.PrintArr("a", a);
		Arr.PrintArr("b", b);
		Arr.PrintArr("c", c);
		Arr.PrintArr("x", x);
		Arr.PrintArr("u", u);
		Arr.PrintArr("v1", v1);
		Arr.PrintArr("v2", v2);
		Console.ReadLine();}}
class Arr
{
	public  static  void  PrintArr(string name, int[] T)
	{
		Console.WriteLine(name);
		for (int i = 0; i < T.GetLength(0); i++)
			Console.Write("\t"    +    name    + "[{0}]={1}", i, T[i]);
		Console.WriteLine();}}*/
	}}
