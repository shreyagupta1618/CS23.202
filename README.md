[Program-1 Write a class for addition of two distances where each distance is given in mm,cm,m. ](#assignment-1) 

[Program-2 WAC for addition of two times where each time is given in hr,min,sec](#assignment-2) 

[Program-3 WAC inheritence](#assignment-3) 

[program-4 WAC with four methods add,subtract,multiply and divide and test all the methods in the main](#assignment-4)

[program-5 WAC for addition of two distances where each distance is given in m and cm](#assignment-5)

[program- 6 WAC for addition of two times where each time is given in hr and min](#assignment6)

[program- 7 WAC to reverse a 1D array.](#assignment7)

[program- 8 WAC with necessary number of methods for numberof matrix operations: transpose,addition,multiplication,sum of two rows, sum of columns and sum of diagonals of the matrix](#assignment8)

[program-9 Collect all 5 codes of C language like factorial, armstrong, palindrome etc and convert them into object oriented in Java and test the result in main](#assignment9)






## assignment-1
```
import java.util.Scanner;

/**
 *
 * @author IBM32
 */
public class distest {

    public static void main(String[] args)
    {
    distance d1=new distance();
    d1.input();
    distance d2=new distance();
    d2.input();
    
    distance d3=new distance();
   d3.add(d1, d2);
   d3.output();
    
    }
}
 






class distance {
    int mtr;
    int cm;
    int mm;
    void input()
    {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter meter : ");
        mtr = sc.nextInt();
        System.out.print("Enter centimeter : ");
        cm = sc.nextInt();
        System.out.print("Enter milimeter : ");
        mm = sc.nextInt();
        }
    void output()
    {
        System.out.println(mtr);
        System.out.println(cm);
        System.out.println(mm);
        
    }
    
    void add(distance o1 , distance o2)
    {
        mtr = o1.mtr+o2.mtr;
        cm = o1.mtr+o2.cm;
        mm = o1.mtr+o2.mm;
        if (mm>=10)
        {mm=mm-10;
        cm=cm+1;
        }
    }
    
    void tes(){
        
    }
}
```
<img width="1280" height="1024" alt="image" src="https://github.com/user-attachments/assets/055db80d-f32e-40de-a942-550e54e292cc" />




## assignment-2
```
import java.util.Scanner;
/**
 *
 * @author IBM32
 */
public class newfile {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        time t1=new time();
        t1.input();
        time t2=new time();
        t2.input();
        time t3=new time();
        t3.add(t1,t2);
        t3.output();
        
    }
    
}

class time{
    int hour;
    int min;
    int sec;
    void input(){
        Scanner sc =new Scanner(System.in);
        System.out.println("Enter hour:");
        hour=sc.nextInt();
        System.out.println("Enter minutes:");
        min=sc.nextInt();
        System.out.println("Enter seconds:");
        sec=sc.nextInt();  
    }
    
    void output(){
        System.out.println("Hours:"+ hour);
        System.out.println("Minutes:"+ min);
        System.out.println("SEconds:"+ sec);
        
    }
    
    void add(time t1,time t2){
        hour=t1.hour+t2.hour;
        min=t1.min+t2.min;
        sec=t1.sec+t2.sec;
        
        if(sec>=60){
            min+=sec/60;
            sec=sec%60;
        }
        
        if(min>=60){
            hour+=min/60;
            min=min%60;
        }
    }
}
```
<img width="1280" height="1024" alt="image" src="https://github.com/user-attachments/assets/24ec6e6d-4a87-427e-abc6-c3f9d18d609a" />

## assignment-3
```
public class inheritance {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        testA a=new testA();
        testB b=new testB();
        testC c=new testC();
        a.fun1();
        b.fun2();
        c.fun3();
        
        
    
    }
    
}

class testA{
    public void fun1(){
        System.out.println("We are in class testA");
    }
}

class testB extends testA{    
    public void fun2(){
        System.out.println("We are in class testB");
    }
}

class testC extends testB{
     public void fun3(){
        System.out.println("We are in class testC");
    }
}
```
<img width="1280" height="1024" alt="image" src="https://github.com/user-attachments/assets/f6ba792f-dc85-4d06-99c6-35cb0f7373cc" />


## assignment-4
```
import java.util.Scanner;

class Operation {

    int a,b;

    void input(){
        Scanner s = new Scanner(System.in);
        System.out.println("Enter first number");
        a = s.nextInt();
        System.out.println("Enter second number");
        b = s.nextInt();
    }
    void add(){
        System.out.println("Addition = " + (a+b));
    }
    void sub(){
        System.out.println("Subtraction = " + (a-b));
    }
    void mul(){
        System.out.println("Multiplication = " + (a*b));
    }
    void div(){
        System.out.println("Division = " + (a/b));
    }
}
public class Calculator {
    public static void main(String[] args) {
        Operation obj = new Operation();
        obj.input();
        obj.add();
        obj.sub();
        obj.mul();
        obj.div();
    }
}   
```

## assignment-5
```
/**
 *
 * @author IBM27
 */
import java.util.Scanner;

public class TimeHM {
    public static void main(String[] args){
        Tt t1 = new Tt();
        Tt t2 = new Tt();
        Tt result = new Tt();
        t1.input();
        t2.input();
        result.add(t1,t2);
        result.output();
    }
}

class Tt{
    int hr,min;
    void input(){
        Scanner s = new Scanner(System.in);
        System.out.println("Enter hours");
        hr = s.nextInt();
        System.out.println("Enter minutes");
        min = s.nextInt();
    }

    void output(){
        System.out.println(hr+" hr "+min+" min");
    }

    void add(Tt t1,Tt t2){
        min = t1.min + t2.min;
        hr = t1.hr + t2.hr;

        if(min>=60){
            hr = hr + 1;
            min = min - 60;
        }
    }
}
```
<img width="578" height="487" alt="image" src="https://github.com/user-attachments/assets/8cadc746-890a-4eb2-970f-8ae99b089335" />


## assignment-6
```
import java.util.Scanner;
/**
 *
 * @author IBM27
 */
public class PalindromeNumber {
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        int num,original,reverse=0,remainder;
        System.out.println("enter a number:");
        num=sc.nextInt();
        original=num;
        while (num!=0){
            remainder=num%10;
            reverse=reverse*10+remainder;
            num=num/10;
            
        }
        if(original==reverse){
            System.out.println("number is palindrome");
        }
        else{
            System.out.println("number is not palindrome");
        }
    }
}
```
