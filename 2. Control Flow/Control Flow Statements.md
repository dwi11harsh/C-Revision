## Switch
- “Case Value” can be of character type and int type.
- There can be one or many number of cases.
- Statements associated with a matching case executes until a break statement is reached.
- The position of default case does not matter. It can be placed anywhere.
- Default case is optional.
- Duplicate case labels are not allowed.
- Statements written before all the cases are ignored by the compiler.
- The break statement is optional.
- Case label cannot be a variable.
```
#include<stdio.h>

int main() 
{
	int i = 1;
	
	switch (i)
	{
		case 1:
			printf("hola");
			break;
		case 2:
			printf("hello");
			break;
		default:
			printf("namaste");
	}
}
```

## For Loop
- It is recommended to use for loop when the number of iterations is known in advance.
- ```for (expression – 1(optional); expression – 2(optional); expression – 3(optional))
{ statement – 1
statement – 2 
.
.
statement – n }```
- If we omit expression-2, the condition is considered as true for an example:
	- ```for ( i = 0 ; ; i ++)
		statement;```
```
#include <stdio.h>

int main()
{
    for ( int i = 1 ; i <= 10 ; i ++ )
    {
        printf("%d\n",i);
    }
}
```

## While Loop
- It is recommended to use for loop when the number of iterations is *not* known in advance.
- Syntax
```
#include<stdio.h>

int main()
{
	int i = 1;

	while (i<=10) 
	{
		printf("%d\n",i);
		i++;
	}
}
```

## Do-while loops
- do while loop check the condition after executing the loop body.
- do while loop body executes at least 1 time, no matter whether the loop termination condition is false or true.
- Syntax
```
#include<stdio.h>

int main()
{
	int i = 1;
	do {
		printf("%d\n",i);
		i ++;
	} while (i<5);
}
```

## Break Statement
- The break statement provides an early exit from loops.
- A break statement causes the innermost loop or switch to be exited immediately.
- main.c
```
#include<stdio.h>

int main()
{
	for ( int i = 0 ; i < 5 ; i ++ ) 
	{
	    printf("before break");
	break;
	printf("after break");
	}
}
```
- output:
```
/tmp/pGngh4uTbe.o
before break

=== Code Execution Successful ===
```

## Continue Statement
- Whenever continue is encountered in a loop, it skips the remaining statement of the current iteration and continues with the next iteration of the loop.
```
#include<stdio.h>

int main()
{
	for ( int i = 0 ; i < 10 ; i ++ ) 
	{
	    if ( i % 2 == 0 )
	    {
	        continue;
	    }
	    printf("%d\n",i);
	}
}
```

## goto Statement
- The **C goto statement** is a jump statement which is sometimes also referred to as an **unconditional jump**  statement. The goto statement can be used to jump from anywhere to anywhere within a function.

```
#include <stdio.h>

void check(int i);

int main() {
    for (int i = 0; i < 5; i++) {
        check(i);
    }
    return 0;
}

void check(int i) {
    if (i % 2 == 0) {
        goto even;
    } else {
        goto odd;
    }

even:
    printf("%3d\teven\n", i);
    

odd:
    printf("%3d\todd\n", i);
    
}
```

