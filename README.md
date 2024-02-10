# test
气泡法
int main()
{
	int a[10], i,k,b;
	for (i = 0;i < 10;i++)
	{
		scanf_s("%d", &a[i]);
	}
	for (k = 9; k >=1; k--)
	{
		for (i = 0;i<k;i++)
		{
			if (a[i] > a[i + 1])
			{
				b = a[i];
				a[i] = a[i + 1];
				a[i + 1] = b;
			}
		}
	}
	for (i = 0;i < 10;i++)
		printf("%5d", a[i]);
}
矩阵对角相加
#include<stdio.h>
int main()
{
	int a[3][3], b, i, j;
	for (i = 0;i < 3;i++)
	{
		for (j = 0;j < 3;j++)
		{
			scanf_s("%d",&a[i][j]);
		}
	}
	b = a[0][0]+a[1][1]+a[2][2];
	printf("%d", b);
}

排序颠倒
#include<stdio.h>
int main()
{
	int a[10], i, k, b;
	for (i = 0;i < 10;i++)
	{
		scanf_s("%d", &a[i]);
	}
	if (a[1] > a[2])
	{
		for (k = 9; k >= 1; k--)
		{
			for (i = 0;i < k;i++)
			{
				if (a[i] > a[i + 1])
				{
					b = a[i];
					a[i] = a[i + 1];
					a[i + 1] = b;
				}
			}
		}
	}
    else
	
		for (k = 9; k >= 1; k--)
		{
			for (i = 0;i < k;i++)
			{
				if (a[i]<a[i + 1])
				{
					b = a[i+1];
					a[i+1] = a[i ];
					a[i] = b;
				}
			}
		}
	

	 for (i = 0;i < 10;i++)
		 printf("%5d", a[i]);
}

鞍点判断
int main()
{
	int a[3][3], i, j;
	for (i = 0;i <3;i++)
	{
		for (j = 0;j < 3;j++)
		{
			scanf_s("%d", &a[i][j]);
		}
	}
	for (i = 0;i < 3;i++)
	{
		for (j = 0;j < 3;j++)
		{
			if (a[i][j] >= a[i][0] && a[i][j] >= a[i][1] && a[i][j] >= a[i][2] && a[i][j] <= a[0][j] && a[i][j] <= a[1][j] && a[i][j] <= a[2][j])
			{
				printf("%5d", a[i][j]);
			}
			else
				printf("没有鞍点");
		}

	}
}
统计字符数
int main()
{
	char a[3][80]; 


	int i, j, A =0,x=0, a1=0,b=0,c=0;
	for (i = 0;i < 3;i++)
	{
		for (j = 0;j < 80;j++)
		{
			a[i][j] = getchar();
			if (a[i][j] >= 65 && a[i][j] <= 90)A++;
			else if (a[i][j] >= 97 && a[i][j] <= 122)x++;
			else if (a[i][j] >= 48 && a[i][j] <= 57)a1++;
			else if (a[i][j] = 32)b++;
			else  c++;



		}
	}
	printf("%5d %5d %5d %5d %5d", A, x, a1, b, c);

}

素数判断
int pn(int x)
{
	int i, judge;
	if (x == 1 || x == 2 || x == 0)
	{
		judge = 1;
	}
	else
	{
		for (i = 2;i < x;i++)
		{
			if (x % i == 0)
			{
				judge = 0;
				break;
			}
			else
			{
				judge = 1;

			}
		}
		return judge;
	}
 
}

最大公因数，最小公倍数
int gcd(int x, int y)
{
	int i, k, gcd;
	if (x > y) k = y;
	else k = x;
	for (i = 1;i <= k;i++)
	{
		if (x % i == 0 && y % i == 0) gcd = i;
	}
	return gcd;
}
int lcm(int x, int y, int z)
{
	int i, k, lcm;
	k = y * z / x;
	for (i = 1;i <= k;i++)
	{
		if (i * x % y == 0 && i * x % z == 0)
		{
			lcm = i * x;
			break;
		}
	}
	return lcm;
}
字符颠倒
void swich(char array[10])
{
	int i, b;
	for (i = 0;i < 5;i++)
	{
		b = array[i];
		array[i] = array[9 - i];
		array[9 - i] = array[i];
	}
}
