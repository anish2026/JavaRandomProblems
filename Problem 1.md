## Code VIT Problem 

```java
import java.util.*;
class Student
{
    public int roll;
    public int mark1;
    public int mark2;
    public int mark3;
    
    Student()
    {
    
    }
    
    Student(int roll,int mark1,int mark2,int mark3)
    {
        this.roll=roll;
        this.mark1=mark1;
        this.mark2=mark2;
        this.mark3=mark3;
    }
    
    
}

public class Main
{
    public static void main (String args[])
    {
        Scanner sc = new Scanner(System.in);
        List<Student> students =new ArrayList<>();
        int n = sc.nextInt();
        int max=0;
        int maxRoll = 0;
        for (int i=1;i<=n;i++)
        {
            int roll= sc.nextInt();
            int mark1 = sc.nextInt();
            int mark2 = sc.nextInt();
            int mark3 = sc.nextInt();
            Student s = new Student(roll,mark1,mark2,mark3);
            students.add(s);
            int total = mark1+mark2+mark3;
            System.out.println(mark1+mark2+mark3);
            if (total>max){
                max=total;
                maxRoll=roll;
            }
        
        }
        
        
    
    int maxx=0;
    int maxxRoll=0;
    for(int i=0;i<n;i++){
        int m1=students.get(i).mark1;
        if(m1>maxx)
        {
            maxx=m1;
            maxxRoll=students.get(i).roll;
        }
        
    }
    System.out.println(maxxRoll+" " +maxx);
        
    maxx=0;
    maxxRoll=0;
    for(int i=0;i<n;i++){
        int m1=students.get(i).mark2;
        if(m1>maxx)
        {
            maxx=m1;
            maxxRoll=students.get(i).roll;
        }
        
    }
    System.out.println(maxxRoll+" " +maxx);
    
      maxx=0;
    maxxRoll=0;
    for(int i=0;i<n;i++){
        int m1=students.get(i).mark3;
        if(m1>maxx)
        {
            maxx=m1;
            maxxRoll=students.get(i).roll;
        }
        
    }
    System.out.println(maxxRoll+" " +maxx);
    
    System.out.println(maxRoll+" "+max);
        
    }  
        
    
}
