# null and void pointer

**Void pointer**- data type ছাড়া pointer কে void pointer বলে। যেকোনো data type এর variable কে void pointer দিয়ে point করা যায় এবং void pointer কে যেকোনো data type এ type cast করা যায়। উল্লেখ্য যে, void pointer দিয়ে dereference করতে হলে অবশ্যই type cast করে নিতে হবে। <mark style="color:red;">**`(int)ptr;`**</mark>

**Null pointer**- যে pointer কোনো memory address এ point করেনা তাকে null pointer বলে। অর্থাৎ, null pointer হলো invalid memory location. <mark style="color:red;">**`int *ptr=NULL;`**</mark>
