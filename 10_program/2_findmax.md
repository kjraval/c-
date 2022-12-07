# code <find max value out of 3>

```
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace findMaxNumber
{
    class Program
    {
        static void Main ( string [] args )
        {
            int [] array = new int [ 3 ];


            for (int i = 0; i < 3; i++)
            {

                Console.Write("Enter array[" + i + "] :");
                array[i] = int.Parse(Console.ReadLine());

            }


            Array.Sort(array);
            Array.Reverse(array);


            Console.WriteLine("max value is :" + array [ 0 ]);

            Console.Read();












        }
    }
}
```
