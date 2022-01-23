#define _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>

int binary_search(int arr[],int k,int sz)
{
	int left = 0;
	int right = sz-1;
	while(left<=right)
	{
		int mid = (left+right)/2;//中间元素的下标
		if(arr[mid] < k)
		{
			left = mid +1;

		
		}
		else if(arr[mid]>k)
		{
			right = mid-1;
		
		}
		else
		{
			return mid;
		}
	
	
	}
	return -1;


}
	




int main()
{    //二分查找，在一个有序数组中查找具体某个数，如果找到了返回这个数的下标，找不到返回-1。
	int arr[] = {1,2,3,4,5,6,7,8,9,10};
	int k = 12;
	int sz = sizeof(arr)/sizeof(arr[0]);//传递过去的是数组arr首元素的地址
	int ret = binary_search(arr,k,sz);
	if(ret == -1)
	{
		printf("找不到指定的数字\n");
		
	
	}
	else
	{
		printf("找到了，下标是：%d\n",ret);
	
	}
	return 0;


}






void Add(int* p)
{
	(*p)++;

}


int main()    //利用函数调用实现--每调用一次函数，sum的值就加一
{
	int sum = 0;
	Add(&sum);
	printf("%d\n",sum);
	Add(&sum);
	printf("%d\n",sum);
	Add(&sum);
	printf("%d\n",sum);
	return 0;
}






int Add(int x,int y)//利用函数调用的方式实现加法运算
{
	int z = x+y;
	return z;


}

int main()
{
	int sum = 0;
	int a = 10;
	int b = 20;
	sum = Add(a,b);
	printf("%d\n",sum);


}