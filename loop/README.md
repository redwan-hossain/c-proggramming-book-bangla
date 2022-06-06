# loop

একই কাজ বার বার করাকে প্রোগ্রামিং এর ভাষায় loop বলে। একটা কন্ডিশন যতক্ষণ না মিথ্যা হবে ততক্ষণ একটা loop চলতেই থাকে এবং প্রতিবার loop রিপিট হওয়াকে iteration বলা হয়।

​

### Loop

loop এর প্রাণ হলো control variable. এটার মান যতক্ষণ true থাকবে ততক্ষণ loop চলবে, যে মূহুর্তে false হয়ে যাবে তখনই loop break হয়ে যাবে। \
আমরা জানি যেকোনো variable এর মধ্যে value থাকে। তাই control variable এর একটা ভ্যালু অবশ্যই থাকতে হবে এবং এই ভ্যালু initialize অংশে সেট করা হয়।\
control variable এর মান true নাকি false সেটা জানার জন্য আমাদের একটা condition প্রয়োজন, তাই relational কিংবা logical operator দিয়ে condition অংশে expression লিখা হয়।\
\
Initialize অংশে control variable এর মান সেট করা হয় এবং condition অংশের expression এর সাহায্যে control variable true নাকি false সেটা যাচাই করা হয়। চমৎকার, আমাদের loop এর দুই-তৃতীয়াংশ শেষ।

\
এখন সমস্যা হলো প্রাথমিক ভাবে control variable true রেখে loop চালু করে দিলেই হবে না, পরবর্তীতে loop থেকে বের হবার জন্য, অর্থাৎ condition অংশ false করার জন্য কিছু একটা করতে হবে। এইজন্য control variable এর মান কে increment অথবা decrement করতে হয় যাতে একসময় condition অংশ false হয়ে loop break হয়ে যায়।

\
তাহলে ব্যাপারটা কি দাড়ালো? প্রথমেই আমরা control variable declare করে একটা value দিয়ে initialize করে নিব। এই অংশটা একবারই execute হবে কারণ এখানে শুধুমাত্র একটা variable এর value সেট করা হয়েছে তাই এই statement এর action এখানেই শেষ। তারপর execute হবে condition অংশ যেখানে true নাকি false সেটা চেকিং হবে। true হলে loop এ ঢুকবে, false হলে loop এর ভেতরে ঢুকবে না। ভেতরে ঢুকার পর statement গুলো execute হবে, তারপর increment/decreement পার্ট execute হবে। \
condition checking- execution of statement inside the loop- increment/decreement এই সার্কেল টা চলতেই থাকবে যতক্ষণ পর্যন্ত condition checking এর output false না হয়।



&#x20; loop parenthesis এর ভেতর boolean expression নেয়।&#x20;

&#x20;`initialization statement- test expression- update statement` এটা একটা loop এর প্রধান প্রসেস।&#x20;

```c
i = 1;   // এখান থেকে initialize হবে। এটাকে iterator বলে।

i<= 10;  // i এর মান test করে দেখবে যে 10 থেকে ছোট বা সমান কিনা।

i++;   // test expression step true থাকা পর্যন্ত update statement চলতে থাকবে।
  
```

&#x20;`i++;` অংশ i এর মান 1 করে করে update করবে, এবং আবার test করে update করবে যতক্ষণ পর্যন্ত i এর ভ্যালু 10 এর বেশি না হবে। অর্থাৎ, 10 এর বেশি হলে test expression মিথ্যা হয়ে যাবে এবং loop ভেঙ্গে যাবে। এটা অনেকটা car racing এর মত, নির্দিস্ট একটা lap থেকে শুরু হবে,  ম্যাক্সিমাম lap লিমিট ক্রস না করা পর্যন্ত racing চলতে থাকবে।

`initialization statement` প্রথমে একবার execute হয় তারপর `test expression` অংশে যায়। যদি `test expression` যদি কখনো false না হয় তাহলে  loop থেকে বের হওয়া যাবে না, এটাকে infinite loop বলে।
