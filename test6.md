#define _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
#include<string.h>
int Fac1(int n)
{	int i = 0;
    int ret = 1;
	for(i=1;i<=n;i++)
	{
		ret *= i;
	
	}
	return ret;

}

int Fac2(int n)
{
	if(n<=1)
		return 1;
	else
		return n*Fac2(n-1);

}






int main()
{
	int jc =3;
	//int a = Fac1(jc);
	//printf("%d\n",a);
	//printf("%d\n",Fac1(jc));
	printf("%d\n",Fac2(jc));

}

int my_strlen(char* str)
{
	if(*str !='\0')
		return 1+my_strlen(str+1);//1.利用递归实现  求字符串长度
	else
		return 0;

}

int my_strlen(char* str)//2.地址得用指针来接收

{	int count = 0;
	while(*str != '\0')//*str是字符串下面对应的数
	{	
		count++;
		str++;
	
	}
	return count;

}


int main()
{
	//利用函数求字符串长度
	char arr[] = "bit";
	int len = my_strlen(arr);//arr是数组，数组传过去的不是整个数组，而是第一个元素的地址
	printf("%d\n",len);

}