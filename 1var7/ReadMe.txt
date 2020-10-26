//Опишите,  используя    Класс,  почтовую  сорти-ровку (город, улица, дом, квартира, кому, цен-ность).  Составьте  программу,  определяющую: 1) сколько посылок отправлено в г. Москву;  2) сколько и куда (список городов)  отправленно посылок  ценностью выше  10 рублей;    3) есть ли  адреса,  куда  отправлено  более  1  посылки, если есть то сколько и кому
using System;
using System.Collections.Generic;
using System.Linq;


public class Program
    {
        public static void Main()
        {
            var list = new List<Post>();
            list.Add(new Post("city1", "street1", 8, 32, "Mike", 34));
            list.Add(new Post("city2", "street2", 5, 33, "Donald", 4));
            list.Add(new Post("city1", "street3", 43, 72, "Tom", 8));
            list.Add(new Post("city3", "street4", 1, 44, "Bob", 3));
            list.Add(new Post("city5", "street5", 3, 1, "Frank", 412));
            list.Add(new Post("city3", "street6", 6, 4, "Lola", 3));
            list.Add(new Post("city5", "street7", 11, 2, "Adam", 60));
 
            
 
            Console.Write(true);
        }
 
        public static int Foo1(string city, List<Post> list) => list.Count(p => p.City == city);
        public static (int, List<string>) Foo2(int price, List<Post> list)
        {
            List<string> cities = new List<string>();
 
            foreach(var post in list)
                if(post.Price > price)
                    cities.Add(post.City);
 
            return (cities.Count, cities);
        }
    }
 
    public class Post
    {
        public Post(string city, string street, int home, int appartment, string to, int price)
        {
            City = city;
            Street = street;
            Home = home;
            Appartment = appartment;
            To = to;
            Price = price;
        }
 
        public string City { get; set; }
        public string Street { get; set; }
        public int Home { get; set; }
        public int Appartment { get; set; }
        public string To { get; set; }
        public int Price { get; set; }
 
        public override string ToString() => $"Город: {City}\nУлица: {Street}\nДом: {Home}\nКвартира: {Appartment}\nКому: {To}\nЦена: {Price}\n";
    }
