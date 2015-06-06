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
