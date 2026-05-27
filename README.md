<img width="990" height="659" alt="SCREEN" src="https://github.com/user-attachments/assets/48697ce3-8518-45c9-83b4-01f23b8fdb9a" />

# Standard Study Case

Complete all filters from Step 1 to Step 9 before proceeding.

## Initial Setup

Choose your execution method:

**Automatic Process:**
1. Navigate to **DISPLAY > MACROS > MATRICE > Execute**
2. The matrix will automatically iterate through LINE 2 PARAMS until the MARKER equals the PIVOT
   - The PIVOT is the value from Step 5 (typically O+ in standard cases, but you can select another matrix point for advanced studies)
   - The ERROR MARGIN is the difference between MARKER and PIVOT
3. When the ERROR MARGIN reaches zero, Step 7 will display STATIC (process complete)

**Manual Process:**
1. Manually adjust the LINE 2 PARAMS value
2. Verify that MARKER equals PIVOT
3. When Step 7 shows STATIC, the process is complete
4. Note: An ERROR MARGIN of approximately 0.01 is acceptable for manual processes

**Cursor Positioning:**
- Move the $ symbol cursor along the vertical line to match the asset's current price on your study date

---

## Reading the Predicted Order Book

### Order Book Sections

The order book is divided into three sections:

| Section | Range | cell |
|---------|-------|-----------|
| **Upper** | Upper price to AOP | L4-L12 |
| **Middle** | Middle AOP to AOP | M12-M19 |
| **Lower** | Lower price to middle AOP | M18-M27 |

### Sub-Ranges and Significant Prices

Each section contains one sub-range with three significant prices:

**Upper Section (L8-L11):**
- Red Price: L8
- Balance Price: L10
- Border Price: L11

**Middle Section (M14-M17):**
- Red Price: M14
- Balance Price: M16
- Border Price: M17

**Lower Section (M20-M23):**
- Red Price: M23
- Balance Price: M21
- Border Price: M20

### Average Order Book Price (AOP)

Each AOP has two prices:

- **Standard AOP:** Upper price (L11) for selling, Lower price (M11) for buying
- **Middle AOP:** Upper price (M18) for selling, Lower price (M19) for buying

---

## How to Open a Trade

### Steps to Identify Entry Points

1. **Get the cursor price** of your asset (SYMBOL $ CELL)
2. **Find the price section** by locating your price in the matrix (SYMBOL $ CELL)
3. **Identify the range** – find the highest price in the UPPER RANGE and the lowest price in the LOWER RANGE after the PIVOT price (H10)
4. **Compare to balance price** – check if the range is above or below the BALANCE PRICE

### Trading Rules by Position

**If Range Approximativly Equals Balance Price:**
- **Case 1:** LOWER RANGE = BALANCE PRICE → Buy at BALANCE PRICE, target RED PRICE
- **Case 2:** UPPER RANGE = BALANCE PRICE → Sell at BALANCE PRICE, target RED PRICE

**If Price is in Upper Section:**
- Range > Balance Price → Check if Case 1 applies; if not, sell at volatility price, target AOP
- Range < Balance Price → Check if Case 2 applies; if not, buy at AOP, target volatility price

**If Price is in Middle Section:**
- Range > Balance Price → Check if Case 1 applies; if not, sell at AOP, target middle AOP
- Range < Balance Price → Check if Case 2 applies; if not, buy at middle AOP, target AOP

**If Price is in Lower Section:**
- Range > Balance Price → Check if Case 1 applies; if not, sell at middle AOP, target volatility
- Range < Balance Price → Check if Case 2 applies; if not, buy at volatility, target middle AOP

---

## Risk Management

**AOPV (Average Order Book Price Volatility)** is the spread between the two AOP values. Use it to manage risk:

### Low Risk
Subtract AOPV from your buy order price, or add AOPV to your sell order price.

### Medium Risk
Set your stop loss at the price level directly adjacent to your order price plus AOPV.

### High Risk
For highly volatile assets:
- **Sell orders:** Set stop loss two price levels above your order price
- **Buy orders:** Set stop loss two price levels below your order price plus AOPV
