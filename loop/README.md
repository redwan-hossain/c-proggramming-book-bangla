# loop

initialization- comparison- update এটা একটা loop এর প্রধান প্রসেস।&#x20;

প্রতিবার loop রিপিট হওয়াকে iteration বলা হয়।&#x20;

```c
i = 1;   // এখান থেকে initialize হবে। 

i<= 10;  // i এর মান compare করে দেখবে যে 10 থেকে ছোট বা সমান কিনা।

i++;   // comparison step যতক্ষণ true থাকবে update process চলতে থাকবে।
  
```

&#x20;`i++;` অংশ i এর মান 1 করে করে update করবে, এবং আবার comparison করে update করবে যতক্ষণ পর্যন্ত i এর ভ্যালু 10 এর বেশি না হবে। অর্থাৎ, 10 এর বেশি হলে comparison এর expression মিথ্যা হয়ে যাবে এবং loop ভেঙ্গে যাবে। এটা অনেকটা car racing এর মত, নির্দিস্ট একটা lap থেকে শুরু হবে,  ম্যাক্সিমাম lap লিমিট ক্রস না করা পর্যন্ত racing চলতে থাকবে।
