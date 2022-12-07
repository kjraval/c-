# Code
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


            int [] [] array = {
    new int[ ] {10, 20, 30},
    new int[ ] {11, 22},
    new int[ ] {88, 99}
    };


            for (int i = 0; i < array.Length; i++)
            {


                for (int j = 0; j < array [ i ].Length; j++)
                {

                    Console.WriteLine(array [ i ] [ j ]);


                }



            }

            Console.Read();



        }
    }
}



```
