# Numbers
Simple program doing simple table calculations.

-----------------------------------------------

using System;



using System.Collections.Generic;


using System.Linq;


using System.Text;



using System.Collections.Generic;
using System.Linq;
using System.Text;

using System.Threading.Tasks;

namespace _06.Test
{
    class Test_6
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());


            var nCopy = n;
            int thirdDigit = n % 10; 
            int firtDigit = n / 10;
            int firstDigit1 = n / 100; 
            int secondDigit = firtDigit % 10;
            
            int Redove = firstDigit1 + secondDigit;
            int koloni = firstDigit1 + thirdDigit;


            int digit5 = 0;
            int digit3 = 0;
            int nelse = 0;


            for (int i = 0; i < Redove; i++)
            {
                for (int j = 0; j < koloni; j++)
                {
                    if (nCopy % 5 == 0)
                    {
                        digit5 = nCopy - firstDigit1;
                        nCopy = digit5;
                        Console.Write(digit5 + " ");
                    }
                   else if (nCopy % 3 == 0)
                    {
                        digit3 = nCopy - secondDigit;
                        nCopy = digit3;
                        Console.Write(digit3 + " ");
                    }
                    else
                    {
                        nelse = nCopy + thirdDigit;
                        nCopy = nelse;
                        Console.Write(nelse + " ");
                    }
                   
                   
                }
                Console.WriteLine();
            }

           
        }
    }
}

