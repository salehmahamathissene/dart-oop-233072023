

\# Dart OOP Assignment: Kigali Bus Card



\*\*Name:\*\* Saleh Mahamat Hisseine  

\*\*Student ID:\*\* 23307/2023



\## My numbers



\- D = 23

\- L = 3

\- Starting balance = 1230 RWF

\- Bus fare = 223 RWF

\- Student discount = 13%



\---



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



\---



\## Part 1: Why no setter for balance?



There is no setter for balance because the balance should not be changed directly. Only the `topUp()` and `pay()` methods should change it. These methods check the transaction before updating the balance. This protects the card balance from invalid changes.



\---



\## Part 2: What does \~/ do?



The `\~/` operator performs integer division. It divides two numbers and returns the whole-number result without the decimal part.



For example:



```dart

print(237 \* 17 / 100);

print(237 \* 17 \~/ 100);

```



The output is:



```text

40.29

40

```



The `/` operator returns a decimal result, while `\~/` returns an integer by removing the fractional part.



\---



\## Part 4: Bug table



| Bug | The line | Why it is wrong (my words) | My fix |

|---|---|---|---|

| 1 | `String \_brand;` and `int \_battery;` | Non-nullable fields must be initialized before they are used. | Initialized `\_brand` with an empty string and `\_battery` with 0. |

| 2 | `SmartPhone(String brand, int battery, String system)` | The child constructor does not pass the required arguments to the parent Phone constructor. | Added `: super(brand, battery)` to call the parent constructor. |

| 3 | `@override void restart()` in SmartPhone | The Phone parent class does not originally have a restart method to override. | Added a `restart()` method to the Phone class. |

| 4 | `p.battery = 100;` | The Phone class originally has no setter for battery. | Added a setter that accepts only values from 0 to 100. |

| 5 | `print(p.battery());` | Battery is a getter, not a method. It cannot be called with parentheses. | Changed it to `print(p.battery);`. |



\### Not a bug



\*\*Line:\*\* `Phone p = new Phone('Tecno', 50);`



This line is correct because the `new` keyword is valid in Dart when creating an object. It is optional, so the object can also be created without it.



\---



\## Part 5: Predict the output



\### My prediction (before running the code)



I predict the program will print:



```text

1

5

```



\*\*Explanation:\*\*



For the first object, `Bag` starts with 0 items. Calling `a.add()` increases the items to 1. Then `a.items = -5` is rejected because the setter only accepts values greater than or equal to zero. Therefore, the first output is 1.



For the second object, `BigBag` overrides the `add()` method and calls `super.add()` twice. Each call increases the number of items by 2. Calling `b.add()` two times gives 4 items. Then `b.items = b.items + 1` increases the value to 5. Therefore, the second output is 5.



\### Real output



```text

1

5

