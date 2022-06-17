# pointer in function

pass by value এর সমস্যা হলো এটা দিয়ে মাত্র একটা value রিটার্ন পাওয়া যায়। কিন্ত pass by reference দিয়ে যতগুলো ইচ্ছা value রিটার্ন করা যায়। তবে pointer রিটার্ন নিয়ে কোনো লাভ নেই কারণ  আগের function রিটার্ন করার পর তার ভেতরের সবকিছু destroy হয়ে যাবে, একই সাথে pointer ও destroy হয়ে যাবে এবং আগের function এর blocked scope এর জন্য main function কিছুই receive করতে পারবে না।&#x20;
