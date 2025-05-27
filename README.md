# Student
    import java.util.*;
    class Student
    {
    int sid;
     String name;
    Student(int sid,String name)
    {
      this.sid=sid;
      this.name=name;
    }
    void putdata()
    {
      System.out.println("Student Id="+sid+"\n"+"Student Name="+name);
    }
    }
    class Marks extends Student
    {
    int m1,m2,m3,m4,m5;
    Marks(int sid,String name,int m1,int m2,int m3,int m4,int m5)
    {
     super(sid,name);
     this.m1=m1;
     this.m2=m2;
     this.m3=m3;
     this.m4=m4;
     this.m5=m5;
     }
    void putmarks()
    {
    System.out.println("Marks 1="+m1+"\n"+"Marks 2="+m2+"\n"+"Marks 3="+m3+"\n"+"Marks 4="+m4+"\n"+"Marks 5="+m5+"\n");
    }
    }
    class Result extends Marks
    {
    Result(int sid,String name,int m1,int m2,int m3,int m4,int m5)
     {
      super(sid,name,m1,m2,m3,m4,m5);
     }
     void calculation()
     {
     int tot=m1+m2+m3+m4+m5;
     float per=tot/5;
     
     char grade;
        if (per >= 90) {
            grade = 'A';
        } else if (per >= 80) {
            grade = 'B';
        } else if (per >= 70) {
            grade = 'C';
        } else if (per >= 60) {
            grade = 'D';
        } else {
            grade = 'F';
        }
     System.out.println("Total="+tot+"\n"+"Percntage="+per+"\n"+"Average Grade="+grade);
     }
    }
    class ResultMain
    {
     public static void main(String args[])
     {
      Scanner s=new Scanner(System.in);
      System.out.println("Enter Student id,name & marks of 5 Subject");
      int sid=s.nextInt();
      String name=s.next();
      int m1=s.nextInt();
      int m2=s.nextInt();
      int m3=s.nextInt();
      int m4=s.nextInt();
      int m5=s.nextInt();
      Result R=new Result(sid,name,m1,m2,m3,m4,m5);
      R.putdata();
      R.putmarks();
      R.calculation();
     
      
     }
    }
    
