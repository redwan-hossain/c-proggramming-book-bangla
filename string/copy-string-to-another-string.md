# copy string to another string

<mark style="color:red;">`#include <string.h>`</mark> এবং  `strcpy(new_array, old_array);` ব্যবহার করে এক string কে আরেক string এ কপি করা যায় তবে এখানেও buffer overflow আছে। তাই এই সমস্যা এড়াতে `strncpy(new_array, old_array, size);` ব্যবহার করতে হয়। `strcpy` behind the scene এ ইনডেক্স ব্য ইনডেক্স replace করে।

```c
a[0] = b[0];
a[1] = b[1];
a[2] = b[2];
যতক্ষণ null character না পাবে এভাবে চলতেই থাকবে।
```

```c
#include <stdio.h>
#include <string.h>

int main() {
  char arr[6] =  "hello";
  char arr2[6] = "world";

  strcpy(arr, arr2);

  printf("%s\n", arr);

  return 0;
}c
```

```c
#include <stdio.h>
#include <string.h>

int main() {
    char string[] = "hello world again";
    char string2[6];
    strncpy(string2, string, 6);
    //copying string
    string2[5] = '\0';

    printf("%s", string2);


    return 0;
}

```
