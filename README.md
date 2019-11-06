# initial-commit
practicing simple java
package lesson3;

public class ex1 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		
		    int x=4;
		    int y=9;
		    int power=1;
		    int i;
		    System.out.println("average:"+((x+y)/2));
		    if(x>y) {
		    System.out.println("big:" + x);
		    }
		    if (x<y) {
		    System.out.println("small:" +y);
		        }
		    for(i=0;i<y;i++) {
		    power=power*x;
		    }
		    System.out.println("power:"+power);
		}
	}
	public class ex2 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
	
		
		   int x=3;
		   int y=5;
		   String Str="hello world";
		   if (x>y) {
		  System.out.println(Str);
		   }
		   if (x<y) {
		  System.out.println(Str);
		   }
		   if (x==y) {
		  System.out.println(Str);
		   }
		   if (x<=y) {
		  System.out.println(Str);
		   }
		   if ((x<=y)&&(x<100)) {
		  System.out.println(Str);
		   }
		}
	}
	public class ex3 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
        int i;
        for (i=0;i<11;i++) {
        	System.out.println(i);
        }
        for(i=10;i>-1;i--) {
        	System.out.println(i);	
        }
        for (i=0;i<11;i++) {
        	System.out.print(i+" ");
        }
        for(i=10;i>-1;i--) {
        	System.out.print(i+" ");	
        }
	}
}
public class ex7 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
        int sum=100;
        int maam=18;
        System.out.println(sum*(maam+100)/100);
        
        int include=118;
        System.out.println(include/(100+maam)*100);
        
        int sumrestaurant=100;
        int tipper=13;
        System.out.println("the wai"
        		+ "ter's tip is: "+(sumrestaurant*(100+13)/100) );
        
        int i=1;
        for(i=1;i<11;i++) {
        	System.out.println("the printed number is: "+ i);
        }
       	}
}


