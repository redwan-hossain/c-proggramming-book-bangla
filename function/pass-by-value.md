# pass by value

pass by value এর মানে হলো main function এ থাকা যেকোনো variable এর মানকে function call এর সময় argument দিয়ে parameter এ পাঠানো।  তাদের মেমোরি লোকেশন আলাদা হয় কারণ parameter এবং argument আলাদা আলাদা ব্লক স্কোপে অবস্থিত তাই function এর ভেতরে কোনো variable এর ভ্যালু manipulated হলেও সেটা ঐ function এর বাইরে এক্সেস করা যায় না। function থেকে কোনো ভ্যালু main function এ আনতে চাইলে অবশ্যই return এর মাধ্যমে আনতে হবে অথবা pointer দিয়ে pass by reference ব্যাবহার করতে হবে।&#x20;
