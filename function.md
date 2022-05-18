# function

> Function call এর সময়কার variable কে argument বলে, অন্যদিকে function declaration এবং definition এর সময়কার variable কে parameter বলে।

```c
#include <stdio.h>

int sumf(int a, int b) {
  int sum = a + b;
  return sum;
}  // function declaration and definition
   // it includes function prototype as well as definition

int subf(int, int);
// function declaration/prototype only

int main() {
  int digit1, digit2;

  scanf("%d %d", &digit1, &digit2);

  int sum = sumf(digit1, digit2);
  int sub = subf(digit1, digit2);
  // calling function and passing argument

  printf("sum-> %d sub-> %d\n", sum, sub);

  return 0;
}

int subf(int x, int y) {
  int left = x - y;
  return left;
}  // function declaration including definition
   // it is worthless because we are declaring function twice
   // only useful for calling function from different file
```
