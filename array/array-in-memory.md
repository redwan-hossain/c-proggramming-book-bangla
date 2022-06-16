# array in memory

একটা array যখন declare করা হয় তখন তার সবগুলো এলিমেন্ট এর জন্য মেমোরিতে জায়গা বরাদ্ধ হয়। array linear data structure হওয়ায় মেমোরিতে element গুলো পাশাপাশি থাকে। কিভাবে থাকে সেটা বোঝার জন্য আমাদের variable size নিয়ে আইডিয়া থাকতে হবে। ধরা যাক, int arr\[5] নামে একটা array declare করা হলো। এর মানে হলো array এর ভেতর পাঁচটা int টাইপের variable তৈরি হয়েছে যেগুলোকে index number দিয়ে access করা যাবে। আমরা জানি, প্রতিটা int টাইপের variable সাধারণত 4 byte জায়গা নেয়। ধরি arr\[0] এর মেমোরি এড্রেস যদি 100 হয় তাহলে  arr এর কাছে শুধু arr\[0] এটার এড্রেস অর্থাৎ 100 থাকবে, বাকিগুলো সে calculation করে নিবে।&#x20;

{% content-ref url="../pointer/array-behind-the-scene.md" %}
[array-behind-the-scene.md](../pointer/array-behind-the-scene.md)
{% endcontent-ref %}

```c
arr[0] = 100
arr[1] = 100+(1*4)= 104
arr[2] = 100+(2*4)= 108
arr[3] = 100+(3*4)= 112
arr[4] = 100+(4*4)= 116
```
