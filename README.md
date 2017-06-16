 #include<iostream.h>
 #include<conio.h>
 class stud
{
	     int tamil,eng,mat,avg;
      public:
	    // friend class stud1;
	       stud()
		{
		 tamil=0;
		 eng=0;
		 mat=0;
		 avg=0;
		 }
	     stud(int t,int e,int m)
		{
		 tamil=t;
		 eng=e;
		 mat=m;
		 avg=totalmark(tamil,eng,mat);
		 }
	     friend int totalmark(int,int,int);
	     friend class stud1;
};
	     int totalmark(int a, int b, int c)
		 {
		 return((a+b+c)/3);
		 }
class stud1
{
	    private:
	     int tamil,eng,mat,avg;
	     public:
		stud1()
		{
		 tamil=0;
		 eng=0;
		 mat=0;
		 avg=0;
		 }
	   stud1(stud obj)
	   {
	    tamil=obj.tamil;
	    eng=obj.eng;
	    mat=obj.mat;
	    avg=obj.avg;
	    }

      void display()
      {
	 cout<<"\ntamil mark is"<<tamil;
	 cout<<"\nenglish mark is"<<eng;
	 cout<<"\nmaths mark is"<<mat;
	 cout<<"\naverage mark is"<<avg; }
};
  int main()
  {
      int s1,s2,s3;
      clrscr();
      cout<<"\nenter the s1 mark :";
      cin>>s1;
      cout<<"\nenter the s2 mark :";
      cin>>s2;
      cout<<"\nenter the s3 mark :";
      cin>>s3;
      stud s01(s1,s2,s3);
      stud1 a(s01);
      a.display();
      getch();
      return 0;
      }
