




//打印九九乘法表
int main()
{	
	//先确认打印九行
	int i = 0;
	for(i = 1;i<=9;i++)
	{	//打印一行
		int j = 0;
		for(j = 1;j<=i;j++)
		{
			printf("%d*%d=%-3d",j,i,i*j);//左对齐
		
		}
			
		printf("\n");
	
	
	}
	return 0;
	

}









int main()
{
	char arr1[] = "00000000000000";
	char arr2[] = "welcome to jia";
	int left = 0;
	int right = strlen(arr1)-1;
	while(left<right)
	{
		arr1[left] = arr2[left];
		arr1[right] = arr2[right];
		printf("%s\n",arr1);
		left++;
		right--;

	}
	
	

	return 0;
}








#include<windows.h>
输入密码，但只有三次机会
int main()
{
	int i = 0;
	char password[20] = {0};
	for(i=0;i<3;i++)
	{	printf("请输入密码");
		scanf("%s",&password);
		if(strcmp(password,"123456")==0)     //等号不能用来比较两个字符串是否相等，应该使用一个库函数。如果相等返回0.
		{	printf("登录成功");
			break;
		}
		
	
	}
	
	if(i == 3)
		printf("三次机会以用完，退出程序");


	return 0;


}







利用二分法查找元素
#define _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
int main()
{
	

	int k = 5;
	char arr[] = {1,2,3,4,5,6,7,8,9,10};
	int sz = sizeof(arr)/sizeof(arr[0]);//计算元素个数
	int left = 0;          //左边数的初始下标
	int right = sz-1;     //右边数的初始下标
	while(left<=right)
	{
		int mid = (left+right)/2;      //中间数的下标
		if(arr[mid]>k)                 //如果中间数的下标比所找值的下标大
		{
			right = mid-1;
		
		
		
		}
		else if(arr[mid] < k)
		{
			left = mid+1;
		
		}
		else
		{
			printf("找到了，下标是：%d\n",mid);
			break;
		
		
		}
	
	
	
	}
	if(left > right)
	{
		printf("找不到\n");
	
	}


}

