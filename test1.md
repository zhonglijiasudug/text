#define _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>


//根据理想体重判断身体状况
int main()
{	
	

	
	int i = 0;
	int ret = 1;
	int j = 0;
	int sum = 0;
	for(j=1;j<=3;j++)
	{	ret = 1;
		for(i = 1;i <=j;i++)
	{
		ret *= i;
		
	}
		sum+=ret;
	
	}

	printf("%d\n",sum);
	return 0;
}

int main()
{

	int i = 0;
	int ret = 1;
	for(i = 1;i < 10;i++)
	{
		ret *= i;
		
	}
	printf("%d\n",ret);
	return 0;

}




	int main()
{

	
	int i = 1;
	while(i<=10)
	{
		if(i==5)
			continue;
		printf("%d",i);//1234死循环
		
	
		i++;
	}
	
	return 0;
}

		






//顺序语句--三数值的调换
int main()
{
	int a,b,c,temp;
	printf("请分别输入abc三个数的值");
	scanf("%d%d%d",&a,&b,&c);
	temp=a;a=b;b=temp;//借助临时语句，注意三个赋值语句前后‘首尾一致’。
	printf("交换后a的值为%d,b是%d,c是%d",a,b,c);

	return 0;
}







//判断一个数是否为质数
int main()
{
	int i = 0;
	while(i<101)
	{ 
		if(i%2==1)
			printf("%d ", i);
		i++;
	
	
	
	}

	return 0;

}
