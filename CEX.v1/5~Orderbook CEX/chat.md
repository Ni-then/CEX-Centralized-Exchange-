# Orderbook

**Orderbook :** Orderbook ek ledger ya book ki tarha hoti hai jismeh asks , bids & qty ki list hoti hai

> **Orderbook** = abhi tk ke sare pending (unmatched) orders ki list

- **Bids :** buyers ke orders (kitne price pe kharidna chahta hai)
- **Asks :** seller ke ordoers (kitne price pe bechna chahta hai)

---

## Limit order vs Market order

**Limit order :** price + qty dono batate hai & order tabhi execute hoga jb us price (ya useh better) price pe koi match milega , match nahi mila to wo orderbook meh pending rahega

**Market order :** qty specify krte hai , and jo abhi best price hai us pe turant khirda orderbook meh set nahi rehta

---

## More deep with in limit and market order

### 1. Partial fill ( limit order)

#### Case 1 : Limit buy 1 BTC @ $90,010

means $90,010 ya usse sasta jahan mile, kharid lo

- $90,005 pe sirf 0.3 BTC available hai → 0.3 BTC kharida gaya
- $90,010 pe 1.2 BTC hai → 0.7 BTC aur kharida gaya
- Total 1.0 mil gaya, **order poora fill**

#### Case 2 : Limit buy 2 BTC @ $90,010

- 90,005 se 0.3 mila, $90,010 se 1.2 mila = 1.5 BTC mila
- Aage $90,020 hai, wo tumhari limit ($90,010) se mehnga hai, to nahi kharidega
- Bacha 0.5 BTC → order book ke bids mein $90,010 pe pending baith jata hai

> isi ko **paritall filled** kehte hai : order ka ek hissa turant execute , baccha hua hissa wait krta hai , jb tk koi seller us price pe na aaye

---

### 2. Slippage (market order)

Tumne kiya: **Market buy 1 BTC** (koi price limit nahi)

Engine sabse sasta ask pehle uthata hai, phir agla:

| Step | Price | Qty | Cost |
|:----:|:-----:|:---:|:----:|
| 1 | $90,005 | 0.3 | $27,001.5 |
| 2 | $90,010 | 0.7 | $63,007 |
| **Total** | | **1.0** | **$90,008.5** |

- Tum soch rahe the best price $90,005 milega
- Par average price mila $90,008.5
- Ye $3.5 ka gap = **slippage**

**Kyun hota hai?** Best price pe qty kam thi, to agle (mehnge) levels se bhi lena pada.