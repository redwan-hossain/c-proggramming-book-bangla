# array behind the scene

ধরা যাক, int arr\[5] নামে একটা array declare করা হলো।  আমরা জানি, প্রতিটা int টাইপের variable সাধারণত 4 byte জায়গা নেয়। ধরি arr\[0] এর মেমোরি এড্রেস যদি 100 হয় তাহলে  arr এর কাছে শুধু arr\[0] এটার এড্রেস অর্থাৎ 100 থাকবে, বাকিগুলো সে calculation করে নিবে। এই কথাগুলো আমরা যখন array নিয়ে আলোচনা করেছি তখন জেনে এসেছি। এখানে <mark style="color:red;">**`arr`**</mark> হলো একটা pointer কারণ এর কাছে <mark style="color:red;">**`arr[0]`**</mark> এর এড্রেস থাকে। Array এর পরবর্তী element এর ভ্যালু print করতে হলে `*(arr+1)` এভাবে লিখতে হয়। data type অনুযায়ী pointer বুঝে যায় তার কত নাম্বার এড্রেসে যেতে হবে।&#x20;

```c
#include <stdio.h>
int main() {
  int arr[2] = {30, 40};
  printf("%d \n", *(arr + 1)); // output is 40

  return 0;
}
```