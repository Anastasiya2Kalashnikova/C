using System;
					
public class Program
{
	public static void Main()
	{
		//Описать процедуру AddLeftDigit(D, K), добавляющую к целому положительному числу K слева цифру D (D — входной параметр целого типа, лежащий в диапазоне 1–9, K — параметр целого типа, являющийся одновременно входным и выходным). С помощью этой процедуры последовательно добавить к данному числу K слева данные цифры D1 и D2, выводя результат каждого добавления.
		int K = 2345;
            int D1 = 9;
            int D2 = 1;
            AddLeftDigit (D1, ref K);
            Console.WriteLine (K);
            AddLeftDigit (D2, ref K);
            Console.WriteLine (K);
        }
 
        public static void AddLeftDigit(int D, ref int K) {
            if(D <= 0 || D > 9 || K <= 0) 
                throw new ArgumentException("Неверное значение параметров");          
            int n = K;
            while (n != 0) {
                n /= 10;
                D *= 10;
            }
            K += D;
	}
}
