# code

```
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace dynamicArrayInput
{
    class Program
    {
        static void Main(string[] args)
        {

            Console.Write("enter array size :");
            int count = int.Parse(Console.ReadLine());

            int[] array = new int[count];


            for (int i = 0; i < count; i++)
            {

                Console.Write("enter value for array[" + i + "] :");
                array[i] = int.Parse(Console.ReadLine());
            }


            foreach (int value in array)
            {
                Console.WriteLine(value);
            }

            Console.Read();







        }
    }
}
```
