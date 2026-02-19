[Program-1 WAP to add three distances ](#assignment-1) 

[Program-2 WAP to add three diffrent timing](#assignment-2) 

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

