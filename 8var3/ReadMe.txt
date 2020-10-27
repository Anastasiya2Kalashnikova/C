using System;
 
namespace ConsoleApplication1
{
    public class Program
    {
        public static void Main(string[] args)
        {
			//Выясните,  есть  ли  в  слове  X  хотя  бы  одна  из букв "к" или "м"
            string word = "кастрюля";
 
            char[] chars = { 'к', 'м' };
            bool searched = FindAnyChar(word, chars);
            DisplayResult(word, searched);
                
            Console.ReadKey();
        }
 
        private static bool FindAnyChar(string word, char[] chars)
        {
            bool searched = false;
            for (int i = 0; i < chars.Length; i++)
            {
                if (word.IndexOf(chars[i]) == 0)
                {
                    searched = true;
                    break;
                }
            }
            return searched;
        }
 
        private static void DisplayResult(string word, bool searched)
        {
            string text = searched == true ? "была найдена одна из букв" : "не была найдена ни одна из букв";
            Console.WriteLine("В слове \"{0}\" {1}", word, text);
		}
	}
}
