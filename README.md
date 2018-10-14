# Top-Intigers
Soft-Uni exercise
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Array_Rotation
{
    class Program
    {
        static void Main(string[] args)
        {
            var n = int.Parse(Console.ReadLine());

            var firstArr = new int[n];
            var secoundArr = new int[n];

            for (int i = 0; i < n; i++)
            {
                var numbers = Console.ReadLine().Split().Select(int.Parse).ToArray();

                if (i % 2 == 0)
                {
                    firstArr[i] = numbers[0];
                    secoundArr[i] = numbers[1];

                }
                else
                {
                    firstArr[i] = numbers[1];
                    secoundArr[i] = numbers[0];
                }
            }

            Console.WriteLine(string.Join(" ", firstArr));
            Console.WriteLine(string.Join(" ", secoundArr));
            
        }
    }
}
