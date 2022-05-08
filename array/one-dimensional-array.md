# one dimensional array

{% hint style="info" %}
One dimensional array initialize করার নিয়ম-
{% endhint %}

```c
int array1[3]= {1,2,3};
```

```c
int array2[ ]= {1,2,3};
//সবথেকে ভালো, কারণ এখানে array size ফিক্সড না।
```

```c
int array3[2];
array3[0] = 1; 
array3[1] = 1;
//সবচেয়ে বাজে এবং বোরিং নিয়ম
```

```c
int array4[variable]; 
for (i=0; i<array4; i++){
scanf("%d", &array4[i]);
}
//যখন ইউজার ইনপুট নিয়ে ডায়নামিকভাবে array ইলিমেন্ট সেট করতে হয় তখন loop দিয়ে করা সুবিধা।
```
