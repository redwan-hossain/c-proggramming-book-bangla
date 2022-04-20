# while loop

নামতা লেখার প্রোগ্রাম-&#x20;

```c
#include <stdio.h>

int main() {
  int desired, number_one, number_two = 1;

  printf("enter a digit: ");
  scanf("%d", &number_one);

  printf("how many times multiply: ");
  scanf("%d", &desired);

  while (number_two <= desired) {
    printf("%d x %d = %d \n", number_one, number_two, number_one * number_two);
    number_two++;
  }
  return 0;
}
```
