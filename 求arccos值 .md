问题描述

　　利用标准库中的cos(x)和fabs(x)函数实现arccos(x)函数，x取值范围是[-1, 1]，返回值为[0, PI]。要求结果准确到小数点后5位。(PI = 3.1415926)

　　提示：要达到这种程度的精度需要使用double类型。

源代码：

```c
#include <stdio.h>
#include <math.h>
int main()
{
	
	double x;
	double i;
	scanf("%lf",&x);
	
	for(i=3.14159;i>=0.00000;i=i-0.00001)
	{
		if(x-cos(i)<1e-5)
		{
			printf("%.5lf\n",i);
			break;
		}
		
	}
		
return 0;
}
```

