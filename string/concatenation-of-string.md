# concatenation of string

<mark style="color:red;">`#include <string.h>`</mark> এবং  `strcat(new_array, old_array);` ব্যবহার করে এক string কে আরেক string এ কপি করা যায় তবে এখানেও buffer overflow আছে। তাই এই সমস্যা এড়াতে `strncat(destination_array, source_array, available_size_in_destination);` ব্যবহার করতে হয়।&#x20;

{% hint style="info" %}
&#x20;strncat ব্যবহার করলে ম্যানুয়ালি null character দিতে হয়না।
{% endhint %}

```c
#include <stdio.h>
#include <string.h>

int main() {
  char string[] = "Hello, ";
  char string2[100];

  printf("Enter your name: ");
  fgets(string2, 99, stdin);
  // safely taking input upto 99 characters

  int size = strlen(string2);
  strncat(string, string2, size);
  // 3rd argument is for how many strings can be added after the first array
  // First array size is not fixed, so we can store as much string as we want

  puts(string);

  return 0;
}
```
