# Relational Operator

দুইটি operand এর মধ্যে তুলনা করতে relational operator `== != <= >= < >` ব্যবহার করা হয়। এদের সবারই দুইটা operand লাগে তাই এরা বাইনারী operator.  এরা হয় true নয়তো false আউটপুট দিবে। তাই দুইটা operand সত্য নাকি মিথ্যা সেটা বের করতে এই operator ব্যবহার করা হয়। এই operator গুলো সবসময় integer এ আউটপুট দেয়, true এর মান 1, false এর মান 0 হয়।

relational operator গুলোর মাঝখানে কোনরকম স্পেস দেয়া যাবেনা, যেমন এখানে `<=` দুইটার মাঝে স্পেস দিলে সেটা ভুল হবে।

![](../.gitbook/assets/relational-op.png)

relational operator দিয়ে কাজ করার সময় সচরাচর গাণিতিক নিয়মের মত ফলাফল নাও পাওয়া যেতে পারে।&#x20;

3 < z < 5 গাণিতিক নিয়ম অনুযায়ী z এর মান অবশ্যই 4 হতে হবে। যদি z এর মান 2 দেয়া হয় তাহলে  গাণিতিকভাবে এটা ভুল হবে কিন্ত C এর নিয়ম অনুযায়ী সত্য হবে। কিভাবে? আমরা জানি < এই অপারেটর এর associativity বাম থেকে ডান দিকে।

```c
3 < 2 <5  // 3 < 2 এটা মিথ্যা
0 < 5     // 0 < 5 এটা সত্য
1         // তাই উত্তর হবে সত্য বা 1 

3 < z && z < 5  
3 < 4 && 4 < 5
// এইভাবে লিখলে গাণিতিক এবং C উভয়ের নিয়মই ঠিক থাকবে।
```

&#x20;



