using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Net;
using System.Text;
using System.Text.RegularExpressions;
using System.Threading.Tasks;
					
public class Program
{
	
		//Описать функцию IsPower5(K) логического типа, возвращающую True, если целый параметр K (> 0) является степенью числа 5, и False в противном случае. С ее помощью найти количество степеней числа 5 в наборе из 10 целых положительных чисел. 
		public static bool IsPower5(int k)
        {
            if(k < 5) return false; //k<0 если считать, что 5^0 = 1
            while(k%5==0)
            {
                k /= 5;
            }
            return k == 1;
        }
        public static void Main(string[] args)
        {
            var array = new int[] { 1, -1, 5, 15, 25, 125, 625, 6, 10, 11 };
            var count = 0;
            for(int i = 0; i < array.Length; i++)
            {
                if(IsPower5(array[i])) count++;
            }
            Console.WriteLine(count);
        }
	
}
