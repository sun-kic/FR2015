#20150711 関数の使い方
~~~c
#include <stdio.h>
int sum(int begin,int end);/*beginからendまでの合計を求める*/

int main()
{
	/*1~10までの合計を計算する、そして、21~40までの合計*/
	/*を計算し、２つの合計値を足す,35~58までの合計を足す*/
	int sum1 = sum(1,10)+sum(21,40)+sum(35,58);
	printf("%d\n",sum1);
	
	return 0;
}

int sum(int begin,int end)
{
	int i;
	int sum=0;
	for (i=begin;i<=end;i++)
	{
		sum = sum + i;
	}
	return sum;
}


~~~

#20150627 基本挿入法
~~~c
#include <stdio.h>

int main()
{
  int i,j,n,temp;
  int t[] = {4,9,1,7,3,2,6};
  for(i=1;i<7;i++)
  {
	j=i-1;
	while(j>=0)
	{
      if(t[j]>t[j+1])
	  {
		temp=t[j];
		t[j]=t[j+1];
		t[j+1]=temp;
		j=j-1;
	  }
	  else
	  {
		j = -1;
	  }
	}
  }
  for(n=0;n<7;n++)
  {
	printf("%d,",t[n]);
  }
  
}
~~~

#20150620 selection sort 
~~~c
#include <stdio.h>

void selsort(int x[],int n);

void selsort(int x[],int n)
{
    int i,j,z,k;
    for(i=0;i<n-1;i++)
     {
	  k = i; 
        for(j=i+1;j<n;j++)
          {
            if(x[k]>x[j])
               {
		   k = j;
               }
          }
	  z = x[i];
	  x[i] = x[k];
	  x[k] = z;
     }
}

int main()
{
   int p;
   int x[]= {9,7,5,12,3,2,8,4,6,1};
   selsort(x,10);
   for(p=0;p<10;p++)
    {
        printf("%d,",x[p]); 
    }
}
~~~

#20150620 Bubsort fuction
~~~c
#include <stdio.h>

void bubsort(int x[],int n);

void bubsort(int x[],int n)
{
    int i,j,z,flag;
    for(i=n-1;i>0;i--)
     {
        flag = 0;
        for(j=0;j<i;j++)
          {
            if(x[j]>x[j+1])
               {
                z=x[j];
                x[j]=x[j+1];
                x[j+1]=z;
                flag = 1;
               }
          }
        if(flag == 0)
          {
            break;
          }
     }
}

int main()
{
   int p;
   int x[]= {9,5,3,8,6,1};
   bubsort(x,6);
   for(p=0;p<6;p++)
    {
        printf("%d",x[p]); 
    }
}
~~~

#20150619 Bubsort
~~~c
#include <stdio.h>

int main()
{
   int i,j,z,p;
   int x[]= {9,5,3,8,6,1};

    for(i=5;i>0;i--)
     {
        for(j=0;j<i;j++)
          {
            if(x[j]>x[j+1])
               {
                z=x[j];
                x[j]=x[j+1];
                x[j+1]=z;
               }
          }
     }
   for(p=0;p<6;p++)
    {
        printf("%d",x[p]); 
    }
}
~~~

#20510613 Score judge sourcecode
~~~c
#include <stdio.h>

// math >90 AND english > 85

int handan(int,int);//0 is OK , 1 is fail.

int handan(int math,int english)
{
    if(math > 90 && english >85)
    {
        return 0;
    }
    else
    {
        return 1;
    }
}

int main()
{
    int m,e;
    printf("please input math score:");
    scanf("%d",&m);
    printf("please input english score:");
    scanf("%d",&e);
    if (handan(m,e) == 0)
    {
        printf("You are a good student!\n");
    }
    else
    {
        printf("I am sorry!\n");
    }
    return 0;
}
~~~

#20510606 C Source Code
~~~c
#include <stdio.h>
int evensum(int,int);
float bmi(float,float);

float bmi(float h,float w)
{
    return w/(h*h);
}
int evensum(int nmin,int nmax)
{
    int sum;
    int n;
    n = nmin;
    sum = 0;
    while(n<=nmax)
    {
        if (n%2==0)
        {
            sum =sum +n;
        }
        n = n + 1;
    }
    return sum;
} 
int main()
{
    float h,w;
    printf("please input your height:");
    scanf("%f",&h);
    printf("please input your weight:");
    scanf("%f",&w);
    float bmicount = bmi(h,w);
    printf("BMI is %f\n",bmicount);
}
~~~

# FR2015
~~~c
#include <stdio.h>

int add(int,int);
float bmi(float,float);
float tax(float,float);

float tax(float money,float rate)
{
	float money1;
	money1 = money + money*rate;
	return money1;
}

float bmi(float h, float w)
{
	return w/(h*h);
}
int add(int x,int y)
{
	return x + y;
}

int main(void)
{
	int i;
	float j;
	float k;
	i = add(5,6);
	j = bmi(1.75,78.3);
	k = tax(100,0.10);
	printf("%d\n",i);
	printf("%f\n",j);
	printf("%f\n",k);
}
~~~
