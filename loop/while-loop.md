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

n থেকে n জোড় সংখ্যার যোগফল বের করার প্রোগ্রাম-

```c
#include <stdio.h>
int main() {
  int start, upto, sum = 0;

  printf("Enter a number: ");
  scanf("%d", &start);

  printf("Upto: ");
  scanf("%d", &upto);

  if (start % 2 != 0) {
    printf("You have entered an odd number.");
    start += 1;
    printf(" the immediate even number is: %d \n", start);
    while (start <= upto) {
      sum = sum + start;
      start = start + 2;
    }
  } else {
    while (start <= upto) {
      sum = sum + start;
      start = start + 2;
    }
  }
  printf("Sum is: %d \n", sum);
  return 0;
}
```

n থেকে n বিজোড় সংখ্যার যোগফল বের করার প্রোগ্রাম--

```c
#include <stdio.h>
int main() {
  int start, upto, sum = 0;

  printf("Enter a number: ");
  scanf("%d", &start);

  printf("Upto: ");
  scanf("%d", &upto);

  if (start % 2 != 1) {
    printf("You have entered an even number.");
    start += 1;
    printf(" the immediate odd number is: %d \n", start);
    while (start <= upto) {
      sum = sum + start;
      start = start + 2;
    }
  } else {
    while (start <= upto) {
      sum = sum + start;
      start = start + 2;
    }
  }
  printf("Sum is: %d \n", sum);
  return 0;
}
```
