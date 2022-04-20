# loop

একই কাজ বার বার করাকে প্রোগ্রামিং এর ভাষায় loop বলে। একটা কন্ডিশন যতক্ষণ না মিথ্যা হবে ততক্ষণ একটা loop চলতেই থাকে এবং প্রতিবার loop রিপিট হওয়াকে iteration বলা হয়।  &#x20;

&#x20;`initialization statement- test expression- update statement` এটা একটা loop এর প্রধান প্রসেস।&#x20;

```c
i = 1;   // এখান থেকে initialize হবে। এটাকে iterator বলে।

i<= 10;  // i এর মান test করে দেখবে যে 10 থেকে ছোট বা সমান কিনা।

i++;   // test expression step true থাকা পর্যন্ত update statement চলতে থাকবে।
  
```

&#x20;`i++;` অংশ i এর মান 1 করে করে update করবে, এবং আবার test করে update করবে যতক্ষণ পর্যন্ত i এর ভ্যালু 10 এর বেশি না হবে। অর্থাৎ, 10 এর বেশি হলে test expression মিথ্যা হয়ে যাবে এবং loop ভেঙ্গে যাবে। এটা অনেকটা car racing এর মত, নির্দিস্ট একটা lap থেকে শুরু হবে,  ম্যাক্সিমাম lap লিমিট ক্রস না করা পর্যন্ত racing চলতে থাকবে।

`initialization statement` প্রথমে একবার execute হয় তারপর `test expression` অংশে যায়। যদি `test expression` যদি কখনো false না হয় তাহলে  loop থেকে বের হওয়া যাবে না, এটাকে infinite loop বলে।
