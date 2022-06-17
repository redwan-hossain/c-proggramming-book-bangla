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

array by default pass by reference অর্থাৎ function এর argument হিসেবে array pass করলে সে value না পাঠায়ে memory address পাঠায়। array যেহেতু function parameter এ behind the scene pointer নিয়ে কাজ করে, তাই <mark style="color:red;">**`int arr[]`**</mark> এর পরিবর্তে চাইলে <mark style="color:red;">**`int *arr`**</mark> লিখা যাবে যেটা <mark style="color:red;">**`arr[0]`**</mark> এর এড্রেস রিসিভ করবে। তাহলে array এর পরবর্তী element গুলোর address কিভাবে পাবে? <mark style="color:red;">**`address_of_arr[0]+(data_type_size*index_no)`**</mark> এই সূত্র অনুযায়ী বাকি element গুলোর address ক্যালকুলেশন হবে।&#x20;

যেহেতু শুধুমাত্র <mark style="color:red;">**`arr[0]`**</mark> এর এড্রেস পাঠানো হয়, কখনো যদি array এর size নিয়ে কাজ করতে হয় তাহলে অবশ্যই parameter এ size টাও পাঠাতে হবে কারণ compiler যানে না যে তাকে size বের করতে বললে কখন থামতে হবে। string এর ক্ষেত্রে null chracter এ গিয়ে compiler থেমে যায় তাই string parameter হিসেবে দিলে size না দিলেও চলবে কিন্ত array তে এই সুযোগ নাই।

```c
#include <stdio.h>

void changeMe(int *arr) {
  // using pointer to receive the address of arr[0]
  // int *arr is similar to int arr[]
  // address_of_arr[0]+(data_type_size*index_no) this is the formula
  // to calculate the next array element's address

  arr[1] = 50;       // traditional norm to access array by index number
  *(arr + 2) = 100;  // accessing array index by pointer
}

int main() {
  int arr[3] = {3, 4, 10};
  changeMe(&arr[0]);  // changeMe(arr);
                      // sending the address of arr[0]
                      // int &arr[0] is similar to arr

  printf("%d %d\n", arr[1], arr[2]);

  return 0;
}
```
