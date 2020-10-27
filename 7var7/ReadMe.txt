
using System;
 

   public class Program
    {
        public static void Main(string[] args)
        {
			//Даны строкиS иS0. Проверить, содержитсяли строкаS0   встрокеS.   Если   содержится, товывести    True,    если    несодержится, товывести False.
            string s = "Колобок повесился.";
            string s0 = "вес";
            bool subString = false;
 
            for(int i = 0; i < s.Length; i++)
            {
                for(int j = 0; j < s0.Length; j++)
                {
                    if (s0[j] != s[i + j])
                    {
                        subString = false;
                        break;
                    }
                    else
                        subString = true;
                }
                if (subString)
                    break;
            }
 
            if(subString)
                Console.WriteLine("Подстрока найдена");
            else
                Console.WriteLine("Подстрока не найдена");
 
             Console.ReadKey();
        }
    }
