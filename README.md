using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Christmas_Hat
{
    class Program
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());

            int sides = (n * 2) - 1;

            Console.WriteLine("{0}/|\\{0}", new string('.', sides));
            Console.WriteLine("{0}\\|/{0}", new string('.', sides));
            for (int i = 0; i < n * 2; i++)
            {
                Console.WriteLine("{0}*{1}*{1}*{0}", new string('.', sides), new string('-', i));
                sides--;
            }
            Console.WriteLine($"{new string('*', (4 * n) + 1)}");
            for (int i = 0; i < (2 * n) + 1; i++)
            {
                Console.Write("*");
                if (i == 2 * n)
                {
                    break;
                }
                Console.Write(".");
            }
            Console.WriteLine();
            Console.WriteLine($"{new string('*', (4 * n) + 1)}");
        }
    }
}
