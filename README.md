# initial-commit
practicing simple java
package lesson5arrays;

/*firstLast6([1, 2, 6]) - true
firstLast6([6, 1, 2, 3]) - true
firstLast6([13, 6, 1, 2, 3]) - false
*/
public class ex1 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
        int[] arr= {1,2,6};
        /*boolean firstlast=false;
        	if ((arr[0]==6)||(arr[arr.length]==6)){
        		firstlast=true;
        		System.out.println(firstlast);
        }*/
    	
        firstlast6(arr);
	}
    public static boolean firstlast6(int arr[]) {
    	if ((arr[0]==6)||(arr[arr.length-1]==6)) {
    		return true;
    	}
        	
        	return false;
    	}
    }
——————————————————
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		//given an array of int,prog returns true if array longer than 1 & first&last component are equal
		int[] arr= {1,2,3,1};
		samefirstlast(arr);
	}
			public static void samefirstlast(int arr[]) { 	
		boolean x=false;
		if ((arr.length>=1)&&(arr[0]==arr[arr.length-1])){
			 x=true;
			}
        for (int i:arr)
        	System.out.print(i);
        
		System.out.println("  "+x);
	}
}
/*החזר מערך int אורך 3 המכיל את 3 הספרות הראשונות של מספר PI
המספר PI הוא 3.14159
פלט :   {3,1,4}.*/
public class ex3 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
    double PI=3.14;
    int [] arr= new int [3];
    piarr(PI,arr);
	}
	    public static void piarr(double PI,int arr[]){
	int i;
	int j=(int) (PI*100);
	    for (i=2;i>=0;i--) {
    	arr[i]=j%10;
    	j=j/10;
    	
       }
    for (int k : arr) {
		System.out.print(k);
	}
		}
}
_______________________________
/*נגיד ש -1 מיד אחריו 3 במערך הוא "מזל רע". תוכנית תחזיר TRUE  אם המערך הנתון מכיל  מספר כזה ב -2 המיקומים הראשונים או 2 האחרונים במערך
//unlucky1([1, 3, 4, 5]) - true
//unlucky1([2, 1, 3, 4, 5]) - false
unlucky1([1, 1, 1]) - false
*/
public class ex4 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
        int[] arr= {1,3,4,5};
        int i;
        boolean unlucky=false;
        for (i=0;i<arr.length-1;i++) {
        	if (i==0 || i==arr.length-2) {
        		compare(arr,i);
               	}
        	else continue;
        }
     
	}
	public static void compare(int[] arr,int i) {
		boolean unlucky=false;
		if(arr[i]==1 && arr[i+1]==3) {
    		unlucky=true;
    	}
		for (int arr1:arr)
			System.out.print(arr1);
		System.out.println(unlucky);
		if (unlucky==true)
			System.exit(0);
		
	}
}
________________________________________
/*בהינתן מערך של אינטים באורך מספר אי-זוגי , החזר מערך חדש בגודל 3  שמכיל את האלמנטים מאמצע המערך. אורך המערך יהיה לפחות 3.
לדוגמה:
midThree([1, 2, 3, 4, 5]) - [2, 3, 4
midThree([8, 6, 7, 5, 3, 0, 9]) - [7, 5, 3
midThree([1, 2, 3]) - [1, 2, 3
*/
public class ex5 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
        int[] arr= {8,6,7,5,3,0,9};
        int i=(arr.length/2)-1;
        int[] midthree = new int[3];
        System.arraycopy(arr, i, midthree, 0, midthree.length);
        for (int arr2 : midthree)
        	System.out.print(arr2);
	}
}
______________________________________
/*בהינתן 2 מערכי int, a ו- b, בכל אורך, יש להחזיר מערך חדש עם האלמנט הראשון של כל מערך. אם כל המערך הוא אורך 0, התעלם ממערך זה.
front11([1, 2, 3], [7, 9, 8]) - [1, 7
front11([1], [2]) - [1, 2
front11([1, 7], []) - [1
*/
public class ex6 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
    int[] a= {1,2,3};
    int[] b= {7,8,9};
    int[] front11=new int[2];
    
    copyfront(a,b,front11);
    
	}
    public static void copyfront(int[] arr,int[] arr1,int[]front11) {
    	int i=0;
    	if(arr.length>0) {
    		front11[i]=arr[0];
    		i++;
    	}
    	if(arr1.length>0) {
    		front11[i]=arr1[0];
    		i++;
    	}
        for(int front:front11)
        	System.out.print(front);
    }
}
______________________________________
/*תוכנית תחזיר מספר מספרים אי-זוגיים במערך 
countEvens([2, 1, 2, 3, 4]) - 3
*/
public class ex7 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
        int[] arr= {2,1,2,3,4};
        int i;
        int count=0;
        for (i=0;i<arr.length;i++) {
        	if(arr[i]%2!=0) {
        		count++;
        	}
        }
        for (int arr1: arr)
        	System.out.print(arr1);
        System.out.println("  - "+count);
	}

}





_______________________________________
/*נתון מערך בגודל יותר מ1 , יש להחזיר הפרש בין מספר הכי גדול למספר הכי קטן
bigDiff([10, 3, 5, 6]) - 7
*/
public class ex8 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
    int[] arr= {10,3,5,6};
    Arrays.sort(arr);
    int bigdiff;
    bigdiff=arr[arr.length-1]-arr[0];
    for(int arr1:arr)
    	System.out.print(arr1);
    System.out.println("  -"+bigdiff);
	}
}
___________________________________
package lesson5arrays;
import java.util.Arrays;
/*החזירו את הממוצע "המרוכז" למערך של מספרים שלמים, שנאמר שהוא הממוצע הממוצע של הערכים, 
 * למעט התעלמות מהערכים הגדולים והקטנים ביותר במערך. 
 * אם יש מספר עותקים של הערך הקטן ביותר, 
 * התעלם מעותק אחד בלבד, ובאותו הדבר לערך הגדול ביותר. 
 * השתמש בחלוקה בינונית כדי לייצר את הממוצע הסופי. 
 * אתה יכול להניח שהמערך אורך 3 ומעלה. 
centeredAverage([1, 2, 3, 4, 100]) - 3
centeredAverage([1, 1, 5, 5, 10, 8, 7]) - 5
*/
public class ex9 {
	public static void main(String[] args) {
		// TODO Auto-generated method stub
    int [] arr= {1,1,5,5,10,8,7};
    Arrays.sort(arr);
    int sum=0;
    int i;
    for(i=1;i<arr.length-2;i++) {
    	sum=+arr[i];
    }
    int centeredavg=0;
    centeredavg=sum/(arr.length-2);  
    for (int arr1:arr)
    	System.out.print(arr1);
    System.out.println(" centered avg is: "+centeredavg);
	}
}
