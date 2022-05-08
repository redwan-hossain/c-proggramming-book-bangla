# nested loop

```c
#include <stdio.h>

int n, row, column;

int main() {
  scanf("%d", &n);

  for (row = 1; row <= n; row++) {
  
    for (column = 1; column <= row; column++) {
    
      printf(" %d", column);
      
    }

    printf(" \n");
  }

  return 0;
}
```



row n পর্যন্ত চলবে। ধরি, n = 5, তাহলে প্রথম লুপ টা 5 পর্যন্ত চলবে প্রতিবারই row এর ভ্যালু 1 করে বাড়বে এবং 1 থেকে শুরু হয়ে 5 পর্যন্ত বাড়বে।

column এর প্রাথমিক ভ্যালু 1 এবং row এর প্রাথমিক ভ্যালুও 1 তাই দ্বিতীয় লুপ টা সত্য হবে চালু হবে এবং column এর ভ্যালু 1 প্রিন্ট হবে। যখনই column এর ভ্যালু বেড়ে গিয়ে 2 হবে তখন লুপ মিথ্যা হয়ে বের হয়ে যাবে। এরপর আবার যখন প্রথম লুপে row এর ভ্যালু বেড়ে 2 হবে তখন দ্বিতীয় লুপ আবারো চালু হবে আগেরবার row এর ভ্যালু 1 হওয়ায় দ্বিতীয় লুপ 1 পর্যন্ত গিয়েই শেষ হয়ে গিয়েছিলো, কিন্ত এবার সে 2 পর্যন্ত যেতে পারবে তাই column এর ভ্যালু 1,2 প্রিন্ট হবে।&#x20;

এভাবে row 5 পর্যন্ত বাড়বে এবং একইসাথে column এর ভ্যালুও 5 পর্যন্ত যেতে পারবে এবং প্রতিবার নতুন লাইনে column এর ভ্যালুগুলো প্রিন্ট হবে। নতুন লাইন প্রিন্ট হবার কোড কিন্ত প্রথম লুপের, সে যতবার লুপ চালাবে সে অনুযায়ী নতুন লাইন তৈরি হতেই থাকবে। _**প্রথম লুপ- দ্বিতীয় লুপ- নতুন লাইন।**_ এখন দ্বিতীয় কোন লুপ না থাকলে প্রথম লুপ  ঠিকই চলবে এবং খালি অবস্থায় নতুন লাইন প্রিন্ট করবে।



```c
#include <stdio.h>

int n, row, column;

int main() {
  scanf("%d", &n);

  for (row = 1; row <= n; row++) {
  
    for (column = 1; column <= row; column++) {
    
      printf(" *");
      
    }

    printf(" \n");
  }
  return 0;
}
```