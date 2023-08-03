```c
#include <stdio.h>

int main(void)
{
    printf("Hello World\n")
    return 0;
}
```

start 문서에 이어 새로운 c파일을 열어 코드를 빌드하면 오류가 뜰 것이다. 이유는 하나의 프로젝트에 한 개 이상의 main 함수가 있기 때문이다. 

전의 main 함수의 이름을 바꾸면 오류 없이 될 것이다.

# ++ 뿔뿔

```c
#include <stdio.h>

int main(void)
{
    // ++ 뿔뿔
    int a = 10;
    printf("a 는 %d\n", a); // 10이 반환됨
    a++;
    printf("a 는 %d\n", a); // 11이 반환됨
    
    
    int b = 20;
    printf("b는 %d\n", ++b); // b = b + 1;, 21이 반환됨
    printf("b 는 %d\n", b++); // 이 코드 다음 줄에서 b + 1 을 실행, 21이 반환됨
    printf("b 는 %d\n", b); // 22가 반환됨
    
    return 0;
}
```

# 반복문

**for문**

```c
#include <stdio.h>

int main(void)
{
    for (int i = 1; i <= 10; i++)
    {
        printf("Hello World %d\n", i );
    }
    return 0;
}
```

**while문**

```c
#include <stdio.h>

int main(void)
{
	int i = 1;
	while (i <= 10)
	{
		printf("Hello World %d\n", i++);
		// i++;
	}

	return 0;
}      
```

**do while문**

```c
#include <stdio.h>

int main(void)
{
	int i = 1;
	do {
		printf("Hello World %d\n", i++);
	} while (i <= 10);

	return 0;
}          
```

# 이중 반복문

```c
#include <stdio.h>

int main(void)
{
	for (int i = 1; i <= 3; i++)
	{
		printf("첫 번째 반복문 : %d\n", i);
		for (int j = 1; j <= 5; j++)
		{
			printf("    두 번째 반복문 : %d\n", j);
		}
	}

	return 0;
}          
```

# 구구단 출력하기

```c
#include <stdio.h>

int main(void)
{
	for (int i = 2; i <= 9; i++)
	{
		printf("%d단 계산 \n", i);
		for (int j = 1; j <= 9; j++)
		{
			printf("     %d x %d = %d\n", i, j, i * j);
		}
	}

	return 0;
}
```

# 별표 출력하기(점점 수가 증가하는 별)

```c
#include <stdio.h>

int main(void)
{
	for (int i = 0; i < 5; i++)
	{
		for (int j = 0; j <= i; j++)
		{
			printf("*");
		}
		printf("\n");
	}

	return 0;
}
```

# 별표 출력하기(거꾸로)

```c
#include <stdio.h>

int main(void)
{
	for (int i = 0; i < 5; i++)
	{
		for (int j = i; j = 5 - 1; j++)
		{
			printf(" ");
		}
        for (int k = 0; k <= i; k++)
		{
			printf("*");
		}
		printf("\n");
	}

	return 0;
}
```

# 프로젝트(피라미드를 쌓아라)

```c
#include <stdio.h>

int main(void)
{
    int floor;
    printf("몇 층으로 쌓겠느냐? ");
    scanf_s("%d", &floor);
	for (int i = 0; i < floor; i++)
	{
		for (int j = i; j = floor - 1; j++)
		{
			printf(" ");
		}
        for (int k = 0; k < i * 2 + 1; k++)
		{
			printf("*");
		}
		printf("\n");
	}

	return 0;
}
```

