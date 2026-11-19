

\# Dart OOP Assignment: Kigali Bus Card



\*\*Name:\*\* Saleh Mahamat Hisseine  

\*\*Student ID:\*\* 23307/2023



\## My numbers



\- D = 23

\- L = 3

\- Starting balance = 1230 RWF

\- Bus fare = 223 RWF

\- Student discount = 13%



\## Output of main.dart



```text

Error: name too short

Owner: Saleh Mahamat Hisseine | Balance: 1230 RWF

Owner: Saleh Mahamat Hisseine | Balance: 1230 RWF

Error: top-up must be 500 to 50000 RWF

Topped up 2000 RWF

Paid 223 RWF

Paid 223 RWF

Owner: Saleh Mahamat Hisseine | Balance: 2784 RWF

Student discount: 28 RWF

Paid 195 RWF

Owner: Saleh Mahamat Hisseine | Balance: 1035 RWF

Student card: 13% off

```



\## Part 1: Why no setter for balance?



There is no setter for balance because the balance should not be changed directly. Only the topUp() and pay() methods should change it. These methods check the transaction before updating the balance. This protects the card balance from invalid changes.



\## Part 2: What does \~/ do?



The \~/ operator performs integer division. It divides two numbers and returns the whole-number result without the decimal part.



For example:



237 \* 17 / 100 = 40.29



237 \* 17 \~/ 100 = 40



The / operator returns a decimal result, while \~/ returns an integer.



\## Part 4: Bug table



To be completed.



\## Part 5



My prediction:



Real output:



Was I right?



