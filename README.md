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
~~~c
