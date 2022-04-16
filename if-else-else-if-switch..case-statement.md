# if, else, else if, switch..case statement

কন্ডিশন True হলে কিছু কোড এবং False হলে অন্য কিছু কোড execution এর জন্য C তে if...else স্টেটমেন্ট ব্যবহৃত হয়। আর nested if..else হচ্ছে প্রধান একটা if যদি true হয় তাহলে ভেতরে আরো কিছু  if condition থাকবে। প্রথম if false হলে তারপর যদি else if থাকে সেটা যাচাই হবে, সেটাও মিথ্যা হলে একদম শেষে else এর কোড execute হবে। তবে যেই মূহুর্তেই true পাওয়া যাবে, তার পর থেকে কোড আর execute হবেনা।  &#x20;

```c
  if (test_expression) {
    // run code if test expression is true

    if (test_expression2) {
      // Statements inside the body of nested "if"
    }
  } else if (test_expression3) {
    // statement(s)
  } else {
    // run code if test_expression, test_expression2 & test_expression3 are false
  }
```

একাধিক statement এর জন্য `{}` দিতে হয়, শুধুমাত্র একটা statement হলে `{}` না দিলেও চলে। if এর পরের immediate statement টা if এর অংশ হিসেবে গণ্য হবে, তারপরের গুলা হবেনা।

![](.gitbook/assets/curly-b.png)



switch এর ভেতর থাকা Constant/Variable অনুযায়ী case  label 1, label 2...... এভাবে সিরিয়ালে চলতে থাকবে যতক্ষণ না একটা true ভ্যালু পাওয়া যায়, কোন true ভ্যালু না পেলে default ভ্যালু execute হবে। প্রতিটা label যতক্ষণ না break লেখা খুজে পাবে, ততক্ষণ পর্যন্ত এর ভেতরে থাকা statement গুলো execute হবে ওই label এর অংশ হিসেবে।&#x20;

```c
switch (expression)
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

ডুপ্লিকেট case লিখা যাবে না।&#x20;

শুধুমাত্র integer allowed.

case label হিসেবে Variable লিখা যাবেনা। তবে MACROS লিখা যাবে।

default যেকোনো জায়গায় লিখা যাবে, chronology maintain করা আবশ্যক না।&#x20;
