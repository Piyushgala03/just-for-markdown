### **ROBO Trading Order Flow (Non-Technical Explanation)**

**Step 1: Start**

* The system is ready to place an order.
* Keep track of how many orders have been placed (max 20).

---

**Step 2: Place an Order**

* The system sends an order to buy a stock according to your instructions.
* It checks the balance and market status before placing the order.

---

**Step 3: Monitor the Order**

* The system keeps checking the status of the order:

  **While the order is “bought but not sold” or still pending:**

  * Wait and keep monitoring.
  * Don’t place the next order yet.

  **If the order is “sold”, “cancelled”, or “rejected”:**

  * Stop monitoring.
  * The order is considered complete.

---

**Step 4: Place the Next Order**

* Once the previous order is complete, the system places the next order.
* Repeat Steps 2–4 until **20 orders have been placed and monitored**.

---

**Step 5: End**

* After 20 orders, or if any order fails, the system stops.
* A report is generated showing how many orders were successfully placed and monitored.

---

### **Flow Diagram (Simple Version)**

```
Start
  │
Place Order → Check Balance & Market
  │
  ▼
Monitor Order Status
  │
  ├─ If Bought but not Sold → Wait & Keep Monitoring
  │
  └─ If Sold / Cancelled / Rejected → Ready for Next Order
  │
Repeat until 20 Orders or Failure
  │
End
```

---

This version is **easy for non-tech people** to understand:

* It clearly shows the **decision points** (“wait” vs “next order”).
* It avoids technical terms like “API”, “unique_order_id”, or “JSON”.
* It emphasizes **“place → wait until sold → next”**.

---
