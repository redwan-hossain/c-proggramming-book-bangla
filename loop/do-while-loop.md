# do while loop

যখন লুপ এর comparison অংশের আগে ভেতরের অংশ একবার হলেও execute হতে হয়, তখন do while loop ব্যাবহার করতে হয়। নিচের কোডে আগে do এর অংশ execute হবে, তারপর loop এর condition চেকিং হবে।

```c
#include <stdio.h>

int main() {
  int i;

  do {
    printf("enter an integer: ");
    scanf("%d", &i);

  } while (i != 0);

  printf("You're free!! \n");

  return 0;
}
```

একই কাজ for loop দিয়ে করলে অনেক কোড redundancy(পুনরাবৃত্তি) হতো।&#x20;

```c
#include <stdio.h>

int main() {
  int i;

  printf("enter an integer: ");
  scanf("%d", &i);

 
  for (int i; i != 0;) {
    printf("enter an integer: ");
    scanf("%d", &i);
    // 2nd time repeat

  }

  printf("You're free!! \n");

  return 0;
}
```

while loop দিয়ে করলেও একই অবস্থা।&#x20;

```c
#include <stdio.h>

int main() {
  int i;

  printf("enter an integer: ");
  scanf("%d", &i);

  while (i != 0) {
    printf("enter an integer: ");
    scanf("%d", &i);
  }

  printf("You're free!! \n");

  return 0;
}
```
