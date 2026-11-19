

\# Dart OOP Assignment: Kigali Bus Card



\*\*Name:\*\* Saleh Mahamat Hisseine  

\*\*Student ID:\*\* 23307/2023



\## My numbers



\- D = 23

\- L = 3

\- Starting balance = 1230 RWF

\- Bus fare = 223 RWF

\- Student discount = 13%



\## Part 1: Why no setter for balance?



There is no setter for balance because the balance should not be changed directly. Only the `topUp()` and `pay()` methods should change it. This protects the balance and allows the program to check each transaction before updating it.



