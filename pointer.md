# pointer

{% hint style="info" %}
Syntax- <mark style="color:red;">`data_type *pointer_name`</mark>
{% endhint %}

Pointer variable এর নিজস্ব data type থাকেনা কারণ এটা অন্য কোনো object এর address কে store করে। তাই pointer declare এর সময় যে `data_type` দিতে হয় সেটা মূলত pointer যাকে point করবে সেটার data\_type.value of operator `*` দিয়ে pointer variable এ যে address জমা রাখা আছে সেই address এর ভ্যালু access করতে কাজে লাগে। যেমন:

```c
int x = 10;
*ptr= &x;
// x variable এর মেমোরি এড্রেস address of operator & 
// এর মাধ্যমে x pointer variable এ জমা হয়েছে।

*ptr = 15;
// *ptr এর কাছে x এর এড্রেস আছে 
//তাই সে address এ থাকা value কেও access করে manipulate করতে পারে।
```



```c
#include <stdio.h>

int main() {
    int *q, *p;
    int i = 5;
    p = &i;
    // p has the address of i
    q = p;
    // now q has the address of i stored in p
    *q = 10;
    // as q has the address of i, we can manipulate the value of i
    printf("%d\n", *p);
    // as both p and q have same memory address from i,
    // printing *p or *q will be the same

    return 0;
}
```
