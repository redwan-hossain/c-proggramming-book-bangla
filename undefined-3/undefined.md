# বুলিয়ান

C তে ডিফল্টভাবে boolean ডাটা টাইপ নাই। `#include <stdio.h>` নামক header ফাইল দিয়ে boolean সাপোর্ট আনতে হয়।

```c
#include <stdbool.h>
#include <stdio.h>

int main() {
  int xx, zz;

  printf("enter xx: ");
  scanf("%d", &xx);

  printf("enter zz: ");
  scanf("%d", &zz);
  
  bool condition = zz > xx;
  printf("%d \n", condition);
  
    return 0;
}
```
