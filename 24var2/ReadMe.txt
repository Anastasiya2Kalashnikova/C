//Опишите, используя Класс, Таблицу дат и событий русской истории. Составте программу выдающую список событий 19
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

					
public class Program
{
	public static void Main()
	{
		//Опишите, используя Класс, Таблицу дат и событий русской истории. Составте программу выдающую список событий 19
		Person  p  =  new  Person(); //  вызов конструктора
			p.Vyvod(); //  вывод  на  экран  введенных данных
			Console.ReadLine();
	}	
		public class Person
	{
		// полякласса(закрытые)
		private string fam; // Фамилия
		private string im; // Имя
private System.DateTime dr; // Дата рож-дения Системная операция преобраования данных
		private double rost; // рост, м
		private int ves; // Вес, кг
		// Конструктор по умолчанию. Ввод полей с контро-лем правильности
		public Person()
		{
			Console.Write("Фамилия ");
			fam = Console.ReadLine();
			Console.Write("Имя ");
			im= Console.ReadLine();
			Console.Write("Дата рождения  "); //Если Дата введена не в формате даты дд.мм.гг, то обра-ботчик исключений выводит дату 01/01/2001
			try
			{
				string s = Console.ReadLine();
				dr = Convert.ToDateTime(s);
			}
			catch(FormatException)
			{
				dr = Convert.ToDateTime("01/01/2001");
			}
			Console.Write("Рост, м ");
			try
			{
				string  s  =  Console.ReadLine(); // надовводитьдесятичнуюзапятую!
				rost = Convert.ToDouble(s); 
			}
			catch(FormatException)
			{
				rost = 1.6;  //если введена буква или символ, выводится средний рост 1 м 60 см.
			}
			Console.Write("Вес, кг");
			try
			{
				string s = Console.ReadLine();
				ves = Convert.ToInt32(s);
			}
			catch(FormatException)
			{
				ves = 50; // если введена буква или символ, вы-водится средний вес 50 кг
			}
		}// Метод -вывод данных на экран
		public void Vyvod()
		{
			Console.Clear(); // очистить экран
			//  для  нетекстовых  переменных  автоматически  вы-зывается метод ToString
			Console.WriteLine("Фамилия "     + this.fam);
			Console.WriteLine("Имя " + this.im);
			Console.WriteLine("Дата рождения "  + this.dr);
			Console.WriteLine("Рост "      + this.rost);
			Console.WriteLine("Вес " + this.ves);
		}
	}
		
		
	}

