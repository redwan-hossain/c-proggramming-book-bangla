# file I/O

manually by terminal- <mark style="color:red;">**`g++ 101.cpp -o 101 && ./101 <in.txt >out.txt`**</mark>

* r- read mode
* w- write mode
* a- write mode without deleting old content
* fopen- file open করা।
* fclose- file close করা।
* fscanf- input file থেকে input read করা।
* fprintf- output ফাইলে output দেয়া।

যখন input file থাকবে না তখন read করতে ঝামেলা করবে, কিন্ত output এর সময় file না থাকলেও সমস্যা নেই কারণ তখন write permission থাকে বিধায় file না থাকলেও তৈরি হয়ে যায়। scanf, printf এর মত file থেকে input এবং file এ output দেয়ার জন্য fscanf, fprintf ব্যবহার করতে হয়। এক্ষেত্রে অতিরিক্ত argument হিসেবে file pointer দিতে হয়- <mark style="color:red;">**`fscanf(inputFile, "%d", &n);`**</mark>

```cpp
#include "iostream"
#include "string"

using namespace std;

int main() {
  FILE *inputFile;
  FILE *outputFile;

  inputFile = fopen("in.txt", "r");
  outputFile = fopen("out.txt", "w");

  if (inputFile == NULL) {
    return 0;
  }

  while (true) {
    char ch = fgetc(inputFile);
    if (ch == EOF) {
      break;
    }
    fputc(ch, outputFile);
  }
  
  fclose(inputFile);
  fclose(outputFile);

  return 0;
}
```



```cpp
#include "iostream"
#include "string"

using namespace std;

int main() {
  FILE *inputFile;
  FILE *outputFile;

  inputFile = fopen("in.txt", "r");
  outputFile = fopen("out.txt", "w");

  if (inputFile == NULL) {
    return 0;
  }

  int n;
  fscanf(inputFile, "%d", &n);
  fprintf(outputFile, "%d", n * n);
  
  fclose(inputFile);
  fclose(outputFile);
  return 0;
}
```
