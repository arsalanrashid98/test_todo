# todo

TODO List app.

## Other Logic based questions
## Note: Please run these logic based questions on any online java compiler. Thanks
## Question 1
Define an array of numbers (use any random numbers). Write a program to print only the even numbers of the array. Do not use any library functions, need to do via for loops only


public class OnlyEvenNum   {  
    public static void main(String args[])   {  
        int num=50;  
            System.out.print("Only Even Number from 1 to "+num+":\n ");
                for (int i=1; i<=num; i++)   {  
                    if (i%2==0)   {  
                        System.out.print(i + "\n");  
            }  
                    
        }  
        
    }
    
}

//OR Manually add value


public class OnlyEvenNum   {  
    public static void main(String args[])   {  
        int num []= {7,4,3,0,2,0,5,2,13,2,0,3};
            System.out.print("Only Even Number from 1 to "+num+":\n ");
                for (int i=1; i<=num.length; i++)   {  
                    if (i%2==0)   {  
                        System.out.print(i + "\n");  
            }  
                    
        }  
        
    }
    
}

///////////////////////////////////////////////////////////////

## Question 2:

Find the maximum consecutive 1's in an array of 0's and 1's.
Example:
a) 00110001001110 - Output :3 [Max num of consecutive 1's is 3]
b) 1000010001 - Output :1 [Max num of consecutive 1's is 1]


public class ConsecutiveOnce{

    public static int countConsectiveOnces(int [] arr) {
        int maxConsectiveOne = 0;
        int start = 0;
        int k = 0;
        int zeroCount = 0;
        
        for (int end = 0; end < arr.length; end++) {
            if(arr[end] == 0) {
                zeroCount++;
            }
            while(zeroCount > k) {
                if(arr[start] == 0) {
                    zeroCount--;
                }
                start++;
            }
            maxConsectiveOne = Math.max(maxConsectiveOne, end-start+1);
        }
        return maxConsectiveOne;
    }
    public static void main(String[] args) {
        int [] arr = {0,0,1,1,0,0,0,1,0,0,1,1,1,0};
        System.out.println(countConsectiveOnces(arr));
    }
}


// OR 2nd output

public class ConsecutiveOnce{

    public static int countConsectiveOnces(int [] arr) {
        int maxConsectiveOne = 0;
        int start = 0;
        int k = 0;
        int zeroCount = 0;
        
        for (int end = 0; end < arr.length; end++) {
            if(arr[end] == 0) {
                zeroCount++;
            }
            while(zeroCount > k) {
                if(arr[start] == 0) {
                    zeroCount--;
                }
                start++;
            }
            maxConsectiveOne = Math.max(maxConsectiveOne, end-start+1);
        }
        return maxConsectiveOne;
    }
    public static void main(String[] args) {
       
        int [] arr = {1,0,0,0,0,1,0,0,0,1};
        System.out.println(countConsectiveOnces(arr));
    }
}

/////////////////////////////////////////////////////////////////////////////////////

## Question 3
Suppose you have an array of 101 integers. This array is already sorted and all numbers in this array are consecutive. Each number only occurs once in the array except one number which occurs twice. Write a js code to find the repeated number.
e.g $arr = array(0,1,2,3,4,5,6,7,7,8,9,10...................);

public class RepeatingNumber    {  
public static void repeated(int x[]){
        int i, j;
        int counter = 0;
        for(i=0 ; i<x.length ; i++ ){
            boolean isRepeat = false;
            for(j=i-1 ; j>=0 ; j--){
                if(x[i] == x[j]){
                    isRepeat = true;
                    counter++;
                }
            }
            if(isRepeat){
                counter = counter+1;
                System.out.println(x[i] + " repeated " + counter + " times");
                counter = 0;
            }
        }
    }

    public static void main(String[] args) {
        int arr []= {1,1,2,1,1,5,47,84,54,98,44,51,54,54,85,24,68,101,101,100};
        repeated(arr);
    } 
}
    
///////////////////////////////////////////////////////////////////////////////////
    
##  Question # 4:
Api does not exist


/////////////////////////////////////////////////////////////////////////////////////

## Question # 05:

Assume there is a object of this format 
var obj = {
 “id” : 4, “name” : “abc”,
 “id” : 10, “name” : “ab2”,
 “id” : 5, “name” : “abc3”,
 “id” : 6, “name” : “abc5”
}
It can be a dictionary or java object, as per your language of choice. But its key/value pair dictionary simply.

Write a code to sort the object by id 
I.e final output should have objected sort by id’s


public class InsertSort {
    
  public static void main (String [] args) {

   int [] array = {4,10,5,6};
   String [] arr = {"id"};
   String [] arry = {"abc","ab2", "ab3", "ab5",};
   //String [] arryy = {"abc"};
   int temp;
   for (int i = 1; i < array.length; i++) {
    for (int j = i; j > 0; j--) {
     if (array[j] < array [j - 1]) {
      temp = array[j];
      array[j] = array[j - 1];
      array[j - 1] = temp;
     }
    }
   }
   for (int i = 0; i < array.length; i++) {
     System.out.println(arr[0] +"\t"+ array[i] +" \t name \t"+ arry[i]);
   }
  }
}


////////////////////////////////////////////////////////////////////////////////////
