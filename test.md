#define _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
//根据理想体重判断身体状况
int main()
{
	
	int tizhong,sex;
	float shengao,lixiangtizhong;

	printf("请分别输入你的身高（cm）、体重（kg）、性别（1/0）\n");
	scanf("%f%d%d",&shengao,&tizhong,&sex);
	if(sex==1)
	{lixiangtizhong=(shengao-80)*0.7;
		if(lixiangtizhong<tizhong)
			printf("boy,你太胖啦，应该减肥啦");
		else
			printf("boy,你很健康，继续保持");
	}
	else if(sex==0)
		{lixiangtizhong=(shengao-70)*0.6;
		if(lixiangtizhong<tizhong)
			printf("girl,你太胖啦，应该减肥啦");
		else
			printf("girl,你很健康，继续保持");

		}	
		
		
}


