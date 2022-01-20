

//利用二分法查找元素
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