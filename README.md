# class-task
using System;
using System.ComponentModel;
using System.ComponentModel.DataAnnotations;
using System.Formats.Asn1;

namespace polymorphism
{
    internal class progrom
    {
        static void Main(string[] args)
        {
            ractangle shape = new ractangle();
            triangle p = new triangle();
            Console.WriteLine("enter the value fisrt side triangle");
            double q = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("enter the value second side triangle");
            double e = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("enter the value third side triangle");
            double r = Convert.ToInt32(Console.ReadLine());
          //  Console.WriteLine("enter the value fourth side triangle");
            //double s = Convert.ToInt32(Console.ReadLine());
            double t= p.Triangle(q,e,r);
            Console.WriteLine($"Area of Triangle : {t}");

            int a = shape.rectangle(3, 5);  
           Console.WriteLine($"Area of Rectangle : { a }" );
            square square= new square();
            Console.WriteLine("enter the vale for square");
            int u=Convert.ToInt32(Console.ReadLine());
           int m= square.Square(u);
            Console.WriteLine($"square is : {m}");
           
            }
        
        public class ractangle { 
           public int rectangle(int a,int b)
            { 
                int result=a* b;
                return result;
            }
        }
        public class triangle
        {
            public double Triangle(double a, double  b, double  c)
            {
              double s =( a + b + c)/2;
                double k = (s * (s - a) * (s - b) * (s - c));
                double result = Math.Sqrt(k);
                return result;
            }
            
            
        }
        public class square
        {
            public int   Square (int a)
            {
                int s = a*a;
                return s;
            }
        }
    }

}
