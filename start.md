# Helloworld

```c
#include <stdio.h>

int main() {
    printf("Hello World \n")
}
```

# 경찰서 조서 쓰기

Microsoft Visual Studio 를 사용해 프로젝트를 생성하고 소스 파일에서 C++파일(.cpp)를 선택한 후 확장자를 `.c`로 설정해서 파일을 생성한다. 

```c
#include <stdio.h>
int main(void){
    printf("Hello World \n");
    return 0;
}
```

에러가 발생하는 경우 파일을 삭제하고 다시 생성해 시도해보세요.

<hr/>

> 변수: 변하는 수
>
> 상수: 변하지 않는 

## 정수형 변수

```c
#include <stdio.h>
int main(void){
    int age = 12;
    printf("%d\w", age);
    return 0;
}
```

`%d`는 어떤 정수형 값을 순서대로 가져온다.

```c
#include <stdio.h>
int main(void){
    int age = 12;
    printf("%d\n", age);
    age = 13;
    printf("%d\n", age);
    return 0;
}
```

주석을 사용하는 방법을 먼저 알아보자.

```c
#include <stdio.h>
int main(void){
    /*int age = 12;
    printf("%d\n", age);
    age = 13;
    printf("%d\n", age);*/
    return 0;
}
```

```c
#include <stdio.h>
int main(void){
    int age = 12;
    printf("%d\n", age);
    //age = 13;
    printf("%d\n", age);
    return 0;
}
```

## 실수형 변수

```c
#include <stdio.h>
int main(void){
   	float f = 46.5f;
    printf("%f\n", f);
    return 0;
}
```

소수점 자릿수를 설정하고 싶으면

```c
#include <stdio.h>
int main(void){
   	float f = 46.5f;
    printf("%.2f\n", f);
    double d = 4.428;
    printf("%.2lf\n", d);
    return 0;
}
```

## 상수

```c
#include <stdio.h>
int main(void){
   	const int year = 2000;
    printf("태어난 년도: %d\n", year);
    year = 4.428; //상수로 선언했기 때문에 재차 선언이 불가함
    printf("태어난 년도: %d\n", year);
    return 0;
}
```

## printf

```c
#include <stdio.h>
int main(void){
   	int add = 3 + 7;
    printf("3 + 7: %d\n", add);
    printf("%d + %d: %d\n", 3, 7, 3 + 7);
    printf("%d x %d: %d\n", 3, 7, 3 * 7);
    return 0;
}
```

## scanf

키보드 입력을 받아서 저장하는 명령어

```c
#include <stdio.h>
int main(void){
   	int input;
    printf("값을 입력하세요: ");
    scanf_s("%d", &input);
    printf("입력값: %d\n", input);
    return 0;
}
```

```c
#include <stdio.h>
int main(void){
   	int one, two, three;
    printf("3개의 정수를 입력하세요: ");
    scanf_s("%d %d %d", &one, &two, &three);
    printf("첫번째 값: %d\n", one);
    printf("두번째 값: %d\n", two);
    printf("세번째 값: %d\n", three);
    return 0;
}
```

```c
#include <stdio.h>
int main(void){
   	int one, two, three;
    printf("3개의 정수를 입력하세요: ");
    scanf_s("%d %d %d", &one, &two, &three);
    printf("첫번째 값: %d\n", one);
    printf("두번째 값: %d\n", two);
    printf("세번째 값: %d\n", three);
    return 0;
}
```

```c
#include <stdio.h>
int main(void){
    // 문자(한 글자), 문자열(한 글자 이상의 여러 글자)
   	char c = 'A';
    printf("%c\n", c);
    return 0;
}
```

```c
#include <stdio.h>
int main(void){
   	char str[256];
    scanf_s("%s", str, sizeof(str));
    printf("%s\n", str)
    return 0;
}
```

## 프로젝트

```c
#include <stdio.h>
int main(void){
   	// 경찰관이 범죄자의 정보를 입수(조서 작성)
    // 이름? 나이? 몸무게? 키? 범죄명?
    char name[256];
    printf("이름이 뭐에요? ");
    scanf("%s", name, sizeof(name));
    
    int age;
    printf("몇살이에요? ");
    scanf_s{"%d", &age};
    
    float weight;
    printf("몸무게는 몇 kg 이에요? ");
    scanf_s("%f", &weight);
    
    double height;
    printf("키는 몇 cm 이에요? ");
    scanf_s("%lf", &height);
    
    char what[256];
    printf("무슨 범죄를 저질렀어요? ");
    scanf_s("%s", what, sizeof(what));
    
    // 조서 내용 출력
    printf("\n\n--- 범죄자 정보 ---\n\n	");
    printf(" 이름    : %s\n", name);
    printf(" 나이    : %d\n", age);
    printf(" 몸무게   : %.2f\n", weight);
    printf(" 키      : %.lf\n", height);
    printf(" 범죄    : %s\n", what);
    return 0;
}
```









