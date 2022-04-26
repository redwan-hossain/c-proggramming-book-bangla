# Operator precedence and associativity

যখন একই expression এ বিভিন্ন precedence লেভেলের অপারেটর থাকে তখন যার highest precedence থাকবে সেটা আগে execute হবে। তবে precedence কে parentheses `( )` দিয়ে explicitly control করা যায়।

```clike
2+3*4 = কত হবে?
3 * 4 = 12
2 + 12 = 14
উত্তর = 14, 20 নয়, কারণ + এর চেয়ে * এর precedence বেশি।

(2+3)*4 = কত হবে?
2 + 3 = 5
5 * 4 = 20
উত্তর = 20, 14 নয়, কারণ ( ) এর precedence সবচেয়ে বেশি।
```

