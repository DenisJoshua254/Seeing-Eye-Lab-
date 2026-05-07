I'll work through Lab 1 systematically, following all three parts as instructed.

---

## 🔬 Part 1: SEE Clearly

**What is the real problem here?**
Market women in urban African markets lose 2–3 hours daily standing in queues because there is no system to communicate when popular items like garri or tomatoes will be available, forcing buyers to arrive early and wait indefinitely rather than plan their time.

**Who is affected?**
1. **Market women / buyers** — lose income-generating hours, suffer physical exhaustion, leave children unsupervised
2. **Vendors** — lose customers who give up and leave before stock arrives; face chaotic rushes when it does
3. **Children and dependents** — left unsupervised or dragged along, missing school or care

**One assumption engineers might make that's WRONG:**
That buyers have smartphones and reliable mobile data — in reality, most women in these markets use basic feature phones or no phone at all, so an app-based solution would exclude the very people it claims to help.

---

## 🔬 Part 2: BREAK It Down**Step 2: Abstract the essential data**

| Essential Data | Why It Matters | What to IGNORE |
|---|---|---|
| Vendor restock time | Tells buyers when to arrive, not before | Vendor's name or stall number |
| Item type (garri, tomatoes, oil) | Different goods attract different buyers | Item's origin farm or brand |
| Estimated queue length | Helps buyers decide whether to wait now or return | Buyers' individual names |
| Supplier truck location / ETA | Triggers the alert before the crowd forms | Truck driver's route history |
| Buyer's proximity to market | Determines how early to send the alert | Buyer's purchasing history |

---

## 🔬 Part 3: BUILD the Recipe

**Chosen pathway: Pathway B — Physical signal system**

*(Rationale: Requires zero technology, zero literacy, zero connectivity — works for everyone in the market today.)*

```
START

  WHEN supplier truck arrives at the market gate
  THEN market gate keeper notes arrival and rings a bell ONCE
  THEN vendor hangs GREEN cloth on stall pole
       → signal meaning: "stock is coming, stay nearby"
  THEN nearby women continue other shopping within market
       → they do NOT queue yet

  WHEN vendor begins physically unloading stock onto stall table
  THEN vendor switches GREEN cloth to YELLOW cloth
       → signal meaning: "queue now, serving in 5 minutes"
  THEN women form single orderly queue at stall

  WHEN vendor has served first 10 customers
  THEN vendor switches YELLOW cloth to RED cloth
       → signal meaning: "stock running low, last chance"

  END WHEN stock is fully sold out → vendor removes cloth entirely

END
```

---

## 📝 Deliverable Summary

**1. Problem statement:**
Market women in urban African markets waste 2–3 hours daily in unpredictable queues because no low-tech system exists to communicate when vendors will restock popular essentials, causing lost income, unsupervised children, and physical exhaustion.

**2. Onion diagram:** rendered above — 4 layers from surface symptom to root constraint.

**3. Algorithm:** Pathway B, 6-step pseudocode using a coloured cloth signalling system requiring zero technology, zero literacy, and zero internet access.
