
/*
write a program to perform menu driven actions with udf in java 
1] addition 
2] substraction
3] multiplication
4] division
5] swapped value
6] print table
7] print armston number beween two values
8] pelidrom
9] print table between two values
10] exit
*/
import java.util.Scanner;

class menudriven {
	
		public static void main(){
			
			Helper myHelper = new Helper();
			myHelper.init();
			
		}
	
	
	
}

class Helper {
	
	Helper(){
	
	
	}
	
		public void init(){
			
		while(true){
				
				System.out.Print("1] addition");
				System.out.Print("2] substraction");
				System.out.Print("3] multiplication");
				System.out.Print("4] division");
				System.out.Print("5] swapped value");
                System.out.Print("6] print table");
                System.out.Print("7] print armston number");
                System.out.Print("8] print palidrom number");
                System.out.Print("9] print table between two values");
                System.out.Print("10] exit");
                System.out.Print("enter Your choice :");
                

                }

                public addition(){

                    int a,b;
                      Scanner myObj = new Scanner(System.in);
                     System.out.print("enter number a:");
                     a =  myObj.nextLine();

                     System.out.print("enter number b:");
                     b =  myObj.nextLine();
                     

                }
			
		}
}
