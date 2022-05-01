# conditional operator

conditional operator হলো ternary operator কারণ এতে তিনটা operand লাগে। C তে একটাই conditional operator আছে যার সিনট্যাক্স হলো- `if expression ? then : else;`

এখানে if এর মধ্যে একটা expression থাকবে যেটা সত্য হলে `then` অংশে থাকা কোড execute হবে এবং মিথ্যা হলে `else` অংশে থাকা কোড execute হবে। নিচে conditional operator ব্যবহার করে দুইটি সংখ্যার মধ্যে বড় সংখ্যাটি প্রিন্ট করার প্রোগ্রাম দেয়া হলো- &#x20;

```c
#include <stdio.h>

int main() {
    int a, b;

    scanf("%d %d", &a, &b);

    a > b ? printf("%d is bigger\n", a) : printf("%d is bigger\n", b);

    return 0;
}c
```
