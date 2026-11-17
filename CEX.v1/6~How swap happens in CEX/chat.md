# Swap & Fees

## Swap kab hota hai

Whenever a swap happens is it b/w

1. two limit order
2. one limit order , one market order
3. two market order (**not possible**)

---

## Market order & fees

When i place the market order to buy the 10 aptos
so when i check my balance so their will be not 10 aptos , there will be 39.982 something , and the remaining money will take exchange as a platform fees

> **Note :** fees us cheez mai kati jaati hai jo hme mili hai

- **Buy** --> APT mila --> fees **APT** meh kaate gi
- **Sell** --> UDST mila --> fees **USDT** mai kaate gi

---

## Example

for ex : aagr mere pass **320 USDT** hai , and mene **40 APT** kharidna chahta hu , **$8** ke hissab seh

`40 X 8 = 320` , fees **0.045%**

### Case 1 : aagr fees direct USDT se kaati jaye

- trade ke liye 320 USDT + fees (0.144 USDT) = **320.144 USDT** chahiye
- means aagr hmare pass sirf 320 USDT hai to **order fail ho jayega** , esliye exchance ko qty kam krni parti hai

> **in short :** user ko hmesha extra USDT balance rakhna parega

### Case 2 : aagr fees API seh kaati jaye

- 320 USDT poora trade mai lg gaye
- 40 APT mai seh **0.018 APT** fees kati , hme mile **39.982 APT**
- Order hmesha chal jata hai , **extra balance ki zarurat nahi**

---

## Why they do this

why they do this bcz

1. **Easy accounting**
2. **Order fail nahi hota**