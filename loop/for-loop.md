# for loop

variable গুলো for loop এর বাইরে ডিক্লেয়ার করলে যেকোনো জায়গা থেকে access করা যায়। বাইরে declare করলে সেটা  globally scoped হয়, আর for loop এর ভেতর declare করলে সেটা সেই loop এর ভেতর locally scoped থাকে।&#x20;

```c
#include <stdio.h>

int main() {
  int desired, number_one, number_two;

  printf("enter a digit: ");
  scanf("%d", &number_one);

  printf("how many times multiply: ");
  scanf("%d", &desired);

  for (number_two = 1; number_two <= desired; number_two++) {
    printf("%d x %d = %d \n", number_one, number_two, number_one * number_two);
  }
  return 0;
}
```

n থেকে n তম সংখ্যার যোগফল বের করার প্রোগ্রাম:

```c
#include <stdio.h>
int main() {
  int i, n, sum = 0;

  printf("Enter a number: ");
  scanf("%d", &i);

  printf("Upto: ");
  scanf("%d", &n);

  for (; i <= n; i++) {
    sum = sum + i;
  }

  printf("Sum is: %d \n", sum);
  return 0;
}
```
