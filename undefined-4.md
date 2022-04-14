# অপারেটর

<details>

<summary> বেসিক  </summary>

operator এর কাজ হলো operand এর উপর বিভিন্ন অপারেশন চালানো। a+b⁠ এখানে a এবং b হলো operand, + হলো operator. operand এবং operator মিলে যে কাজ করে তাকে expression বলে। C তে প্রতিটা expression এর শেষে সেমিকোলন দিতে হয়। সাধারণত expression এর মাধ্যমে variable এ ভ্যালু store করা হয়। expression এর আউটপুট constant ভ্যালু হয়।

</details>

<details>

<summary>L Value, R Value</summary>

lvalue মানে হলো এটা data store করতে পারে, এর একটা মেমোরি এড্রেস আছে, এবং এটা অবশ্যই একটা variable হবে, কোনোরকম constant, expression, function হবে না।

rvalue তে কোনোরকম data store করার সক্ষমতা থাকেনা, এগুলো constant, expression, function হয়।

</details>

<details>

<summary>Token Generation</summary>

Compilation process এর প্রথম ধাপ Lexical analysis. Lexical analyzer(source code স্ক্যান করে)  token এ কনভার্ট করে (যদি lexemes পাওয়া যায়)।  lexemes=  meaningful sequence of characters. C তে বিভিন্ন ধরনের token আছে। যেমন:    &#x20;

```
1) Keywords: 
Examples- for, while, if etc.

2) Identifier
Examples- Variable name, function name etc.

3) Operators:
Examples- '+', '++', '-' etc.

4) Separators:
Examples- ', ' ';' etc
```

<img src=".gitbook/assets/Screenshot from 2022-04-14 16-56-46.png" alt="" data-size="original">

</details>

<details>

<summary>Arithmetic operator <mark style="color:orange;"><code>+ - * / %</code><code>⁠</code></mark></summary>

`*` `/` `%` এর অগ্রাধিকার (precedence) বেশি ( associativity বাম থেকে ডানে), এরপরের সিরিয়ালে আসবে `+` `-` (associativity বাম থেকে ডানে)। precedence একই লেভেলের হলে associativity দিয়ে হিসাব হয়। `*` `/` `%` এরা একই লেভেলের, এদের মধ্যে যে বামদিকে আসবে তার কাজই আগে হবে।

`/` এর মাধ্যমে Quotient বের হয়, `%` এর মাধ্যমে Remainder বের হয়।

</details>

<details>

<summary>Increment and Decrement operator <mark style="color:orange;"><code>++ --</code></mark></summary>

এইগুলো একটা ভেরিয়েবলের ভ্যালুকে এক করে বাড়ায় বা কমায়। ধরি `a = 5;` সুতরাং, `a++` এর মানে হলো `a = a + 1;`

এই operator গুলোর সাথে **rvalue** দেয়া যায় না। `a++` হলো `a = a + 1;` এখানে `a` হলো lvalue, `a+1` হলো rvalue `(a+b)++` দিলে `(a+b)=(a+b)+1` হবে। এখানে বামদিকে `(a+b)` একটা  rvalue যেটা data store করতে পারেনা, এজন্য Increment এবং decrement operator এর সাথে rvalue দেয়া যায় না।

&#x20;`++a` হলো **pre-increment operator**. a = 5; এবং x = a++; দিলে x এর value হিসেবে আগে 5 assign হবে, তারপর a এর ভ্যালু increment হবে। এটা কোনো ভ্যারিয়েবলে ডাটা  assign এর সময়কার নিয়ম। &#x20;

```c
#include <stdio.h>  
  
int main()  
{  
  int a = 5;  
  int x;
  
    x = a++;  
  
    printf("x = %d\n", x); 
		
    // output x = 5, not 6 
  
  return 0;  
}
```



`a++` হলো **post-increment operator**, a = 5; এবং x = ++a; হলে এখানে আগে a এর ভ্যালু increment হয়ে 6 হবে, এবং তারপর x এর value হিসেবে assign হবে। এটাও কোনো ভ্যারিয়েবলে ডাটা  assign এর সময়কার নিয়ম। &#x20;

```c
#include <stdio.h>  
  
int main()  
{  
  int a = 5;  
  int x;
  
    x = ++a;  
  
    printf("x = %d\n", x); 
		
    // output x = 6, not 5
  
   return 0;  
}
```

</details>
