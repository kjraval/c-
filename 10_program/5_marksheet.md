# Code <Advance Marksheet>
  
  ```using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace findMaxNumber
{
    class Program
    {
        static void Main ( string [] args )
        {



            Result result = new Result();
            result.createResult();

            


        }
    }
}



class Result
{
    public string name;
    public string rollno;
    public int [] marks;
    public int percentage;
    //constructor
    public Result ()
    {

        name = null;
        rollno = null;
        marks = new int [ 3 ];
        percentage = 0;
      
    }


  void setName(){

      Console.Write("Enter your name :");
     this.name = Console.ReadLine();
   }

  void setRollNo ()
  {

      Console.Write("Enter your roll no :");
      this.rollno = Console.ReadLine();
  }


  void setMarks ()
  {

      Console.Write("Enter your maths mark :");
      this.marks[0] = int.Parse(Console.ReadLine());

      Console.Write("Enter your science mark :");
      this.marks [ 1 ] = int.Parse(Console.ReadLine());

      Console.Write("Enter your english mark :");
      this.marks [ 2 ] = int.Parse(Console.ReadLine());
 
 
  }

  int getTotal ()
  {

      return this.marks [ 0 ]+ this.marks[1]+ this.marks[2];
  }


  float getPercentage ()
  {
      return this.getTotal() / 3;
  }

  bool isPass ()
  {
      int [] marks = this.marks;
      Array.Sort(marks);

      if (marks [ 0 ] < 28)
      {
          return false;
      }
      else
      {
          return true;
      }

  }

  string getRank ()
  {
      if (this.getPercentage() >= 80)
      {
          return "Distiction";

      }
      else if (this.getPercentage() >= 70)
      {

          return "First Class";
      }
      else if (this.getPercentage() >= 60)
      {

          return "Second Class";
      }
      else if (this.getPercentage() >= 50)
      {

          return "Pass Class";
      }
      else
      {

          return "Fail";
      }


  }


  public void createResult ()
  {

      this.setName();
      this.setRollNo();
      this.setMarks();

      if (this.isPass() == false)
      {
          Console.WriteLine("Result : Fail");
      }
      else if (this.getRank() == "Fail")
      {
          Console.WriteLine("Result : Fail");
      

      }
      else
      {

          Console.WriteLine("Result : Pass");
          Console.WriteLine("Total  Marks :" + this.getTotal() + "/" + this.marks.Length *100);
          Console.WriteLine("Percentage is :" + this.getPercentage());
          Console.WriteLine("Rank is :" + this.getRank());
          Console.Read();


      }


  }



}```
