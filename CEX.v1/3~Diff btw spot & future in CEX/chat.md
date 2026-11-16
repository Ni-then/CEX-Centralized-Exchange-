# Spot vs Future

## Spot

**Spot :** BTC kharida
wo hmare balance meh add aa jate hhai
price increase ==> profit & vice-versa

---

## Future

**Future :** BTC buy nahi krte , wo ek contract lete hai ki price kis direction main kayega

- **Long :** price upar jayega
- **Short :** price neeche jayega

### Example of Future trading:

- Entry: BTC $89,000
- Price gaya $90,000 → profit = $1,000 per BTC
- Price gira $88,000 → loss = $1,000 per BTC

---

## Why futures bcz of leverage

**Leverage :** exchange hme udhaar deta hai , taaki hm apne paise seh bada trade kr ske

### setup :

- I have $1000 (isko **margin** kehte hai)
- 10x leverage : exchange seh $9000 uddhar deta hai
- now abh hmare pass $10,000 ka BTC position khol geya hai

### Case 1: Price 1% badha

- $10,000 ka 1% = $100 profit
- Tumhare $1,000 pe $100 = 10% return
- Agar leverage nahi hota (spot), $1,000 pe 1% = sirf $10 profit

### Case 2: Price 1% gira

- $10,000 ka 1% = $100 loss
- Tumhare $1,000 mein se $100 gaye = 10% loss

### Case 3: Price 10% gira (liquidation)

- $10,000 ka 10% = $1,000 loss
- Tumhara poora margin ($1,000) khatam
- Exchange apna $9,000 udhaar wapas bachane ke liye tumhara position zabardasti band kar deta hai. Isko **liquidation** kehte hain.

> **Simple analogy :** Tumne ₹1 lakh ka ghar liya, ₹10,000 apne diye aur ₹90,000 loan. Ghar ka rate 10% gira to tumhare ₹10,000 poore gaye, aur bank ghar le leta hai.

---

## What is liquidation

**Liquidation** = exchange tumhara futures position zabardasti band kar deta hai, kyunki tumhara margin (apna paisa) lagbhag khatam ho gaya.

### Kyun karta hai?

Exchange ne tumhe udhaar diya hai. Agar loss itna badh jaye ki tumhara margin udhaar ko cover na kar sake, to exchange ka paisa doobne ka risk hota hai. Isliye wo position automatically close kar deta hai, pehle hi.

### Example:

- Margin: $1,000, 10x leverage, position $10,000 ka (Long)
- BTC girta hai: loss badhta jata hai
- Jab loss ~$1,000 ke paas pahunchta hai (price ~10% neeche), exchange bol deta hai "bas, ab band"
- Position close, tumhara $1,000 gaya, exchange ka $9,000 safe

### Tumhare liye matlab:

- Margin zero ho jata hai
- Tum koi order nahi dete, sab automatic hota hai
- Baad mein price wapas upar bhi aa jaye, tumhe kuch nahi milta kyunki position pehle hi band ho chuka

### Bachne ke tareeke:

- Kam leverage lo (2x-3x)
- Stop-loss lagao (apni marzi se pehle hi band karo)
- Extra margin daalo (liquidation price door chali jati hai)

> **Simple analogy :** Tumne dost se paise udhaar lekar shares kharide. Shares gir gaye, to dost bolta hai "mere paise abhi wapas de, warna aur nuksaan hoga" aur tumhare shares bech deta hai. Wahi liquidation hai.

---

## Note

**Note :** jitna leverage yada hota etna hi liquidaton ke chance jyada hoge

**why ? :** Leverage zyada = tumhara apna paisa (margin) ka hissa utna hi chota hai , means aagr kabhi bhe loose huya toh hmara margin jaldi reduce ya khtm ho jayega then liquidation happens

### Formula

```
liquidation distance ≈ 100 ÷ leverage (%)
```

- 10x → 100 ÷ 10 = 10%
- 50x → 100 ÷ 50 = 2%

### Example 1: 10x

- Position: $10,000
- Tumhara margin: $1,000 (10%)
- Price 10% gira → $1,000 loss → margin khatam → liquidation

### Example 2: 50x

- Position: $10,000
- Tumhara margin: sirf $200 (2%)
- Price 2% gira → $200 loss → margin khatam → liquidation

> **Note :** Dono mein position same ($10,000) hai, lekin 50x mein tumhara paisa kam laga hai, to cushion (bachav) bhi kam hai.