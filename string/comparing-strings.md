# comparing strings

ছোট string এর সব character বড় string এর সমান হলে সেটাকে বলা হয় prefix. ছোট string বড় string এর prefix হলে বড় string কে বড় বলে ধরে নেয়া হয়।

string কে lexicographical order(ডিকশনারি এর মতো) এ সাজানো যায়।&#x20;

```c
যখন উভয় string এর index সমান হয় তখন:
is a[0] = b[0]? সত্য হলে সামনে আগাবে। 
is a[1] = b[1]? সত্য হলে সামনে আগাবে। 
is a[2] = b[2]? সত্য না হলে থেমে যাবে। 
এরপর lexicographical order দেখবে কে ছোট। 
যে string এ ছোট index value পাবে সেটাকেই ছোট বলে নির্ধারণ করা হবে।
```

{% hint style="info" %}
find first mismatch

if both string ends without mismatch, they are equal

if one of the string ends, that will be short

if no string ends,&#x20;
{% endhint %}

strcmp&#x20;

{% hint style="info" %}
if output is negative, 1st string smaller

if output is 0, equal

if output is positive, 2nd string smaller
{% endhint %}
