# switch statement

switch statement একটা variable থাকে, এখানে এক্সপ্রেশন দেয়া যায় না। case এর ক্ষেত্রে switch এ থাকা variable এর মান হিসেবে constant value দিতে হয় এবং তারপর colon দিয়ে কিছু statement লিখা যায় এবং statement শেষ হলে break দিয়ে দিতে হয় যাতে statement execution শেষে switch statement থেকে বের হওয়া যায়। default হিসেবে একটা option রাখতে হয় যেটা কোনো case match না হলে execute হবে, যেটা অনেকটা else এর মত। default যেকোনো জায়গায় লিখা যাবে, chronology maintain করা আবশ্যক না।&#x20;

switch এর ভেতর থাকা Constant/Variable অনুযায়ী case  label 1, label 2...... এভাবে সিরিয়ালে চলতে থাকবে যতক্ষণ না একটা true ভ্যালু পাওয়া যায়, কোন true ভ্যালু না পেলে default ভ্যালু execute হবে। প্রতিটা label যতক্ষণ না break লেখা খুজে পাবে, ততক্ষণ পর্যন্ত এর ভেতরে থাকা statement গুলো execute হবে ওই label এর অংশ হিসেবে।&#x20;

{% hint style="danger" %}
ডুপ্লিকেট case লিখা যাবে না।  case label হিসেবে Variable লিখা যাবেনা। তবে MACROS লিখা যাবে।
{% endhint %}



```c
switch (variable)
​{
    case constant1:
      // statements
      break;

    case constant2:
      // statements
      break;
    .
    .
    .
    default:
      // default statements
}
```
