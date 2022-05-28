# static function

যেকোনো user defined function ডিফল্ট ভাবে global scoped হয়। এই কারণে অন্য ফাইল থেকেও যেকোনো function কে access করা যায়। অন্য ফাইল যাতে access না পায় এজন্য একটা user defined function static keyword দিয়ে ডিক্লেয়ার করলে সেটা শুধুমাত্র সেই ফাইলের ভেতরেই global scoped হবে, বাইরে থেকে একে access করা যাবেনা।  static function এর এই সুবিধার জন্য একই নামের function অন্য ফাইলের ভেতর বানানো যাবে।
