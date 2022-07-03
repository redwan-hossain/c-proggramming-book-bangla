# array of structure

primitive data type এর যেমন array হতে পারে, তেমনিভাবে user-defined data type এর ও array হতে পারে, যেমন array of structure।

```c
#include <stdio.h>
struct student { 
  char name[50];
  int marks;
  int roll;
}; // 

int main(){

struct student arr[3];
// এখানে খুবই চমৎকার ভাবে student type এর তিন টা array তৈরি হয়ে গেলো।

return 0;
}
```
