# Code

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

            int col, row;

            Console.Write("Enter colum for your array :");
            col = int.Parse(Console.ReadLine());

            Console.Write("Enter row for your array :");
            row = int.Parse(Console.ReadLine());


            int[,] array = new int[col, row];



            for (int i = 0; i < col; i++)
            {

                for (int j = 0; j < row; j++)
                {
                    Console.Write("enter array[" + i + "," + j + "] :");
                    array[i, j] = int.Parse(Console.ReadLine());
                }

            }


            while (true)
            {
                Console.Clear();
                Console.WriteLine();
                Console.WriteLine("0] exiit");
                Console.WriteLine("1] addition");
                Console.WriteLine("2] substraction");
                Console.WriteLine("3] multiplication");
                Console.WriteLine("4]  division");
                Console.Write("enter your choice :");
                int choice = int.Parse(Console.ReadLine());


                if(choice == 0) break;

                switch (choice)
                {
                        
                

                    case 1:
                        {
                            int total = 0;

                            foreach (int value in array)
                            {
                                total = total + value;
                            }

                            Console.Write("Addition is :" + (total));
                            Console.Read();
                            break;
                        }

                    case 2:
                        {
                            int total = 0;

                            foreach (int value in array)
                            {
                                total -= value;
                            }

                            Console.Write("Substraction is :" + total);
                            Console.Read();
                            break;
                        }
                    case 3:
                        {
                            int total = 1;

                            foreach (int value in array)
                            {
                                total *= value;
                            }

                            Console.Write("Multiplication is :" + total);
                            Console.Read();
                            break;
                        }
                    case 4:
                        {
                            int total = 1;

                            foreach (int value in array)
                            {
                                total /= value;
                            }

                            Console.Write("Division is :" + total);
                            Console.Read();
                            break;
                        }

                    default: {

                        Console.Write("Invalid option selected");
                        Console.Read();
                        break;

                    }

                  





                }





            }
            


            Console.Read();


        }

      
    }
}

```
