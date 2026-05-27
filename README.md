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

## How to Read the Predicted Order Book

### Order Book Sections

     The order book is divided into three sections:
     •	UPPER SECTION between upper price and AOP   [L4-L12]
     •	MIDDLE SECTION between middle AOP and AOP   [M12-M19]
     •	LOWER SECTION  lower and middlle AOP        [M18-M27]

     Every section contains ONE sub-range WITH THREE SIGNIFICANT PRICES
     •	SUB UPPER SECTION  [L8-L11]  (RED PRICE = L8  ; BALANCE PRICE = L10 ; BORDER PRICE = L11 )
     •	SUB MIDDLE SECTION [M14-M17] (RED PRICE = M14 ; BALANCE PRICE = M16 ; BORDER PRICE = M17 )
     •	SUB LOWER SECTION  [M20-M23] (RED PRICE = M23 ; BALANCE PRICE = M21 ; BORDER PRICE = M20 )

### Average Order Book Price (AOP)

     Each AOP has two prices:
     •	AOP : Upper price (L11) for selling, Lower price (M11) for buying
     •	Middle AOP : Upper price (M18) for selling, Lower price (M19) for buying

---

## How to Open a Trade

### Steps to Identify Entry Points

1. **Get the cursor price** of your asset (SYMBOL $ CELL)
2. **Find the price section** by locating your price in the matrix (SYMBOL $ CELL)
3. **Identify the range** – find the highest price (UPPER RANGE) and the lowest price (LOWER RANGE) after the PIVOT price (H10)
4. **Compare to balance price** – check if the range is above or below the BALANCE PRICE

### Trading Rules by Position

- THE RANGE IS CONTAINED IN A SINGLE SECTION

**TREND USED TO BREAK AT BALANCE PRICE**

     •	case 1 : If LOWER RANGE = BALANCE PRICE → Buy  BALANCE PRICE target RED PRICE
     •	case 2 : If UPPER RANGE = BALANCE PRICE → Sell BALANCE PRICE target RED PRICE

**CURSOR PRICE IN UPPER SECTION** 

     •	RANGE > BALANCE PRICE : Check if Case 1 applies if not sell at volatility price target AOP 
     •	RANGE < BALANCE PRICE : check if case 2 applies if not buy at AOP price target volatility   

**CURSOR PRICE IN MIDDLE SECTION** 

     •	RANGE > BALANCE PRICE : check if case 1 applies if not sell at AOP price target middle AOP 
     •	RANGE < BALANCE PRICE : check if case 2 applies if not buy at middle AOP target  AOP price  

**CURSOR PRICE IN LOWER SECTION**

     •	RANGE > BALANCE PRICE : check if case 1 applies if not sell at middle AOP target volatility
     •	RANGE < BALANCE PRICE : check if case 2 applies if not buy at volatily price target middle AOP  

**PRICE OSCILLATES ON EITHER SIDE OF THE BALANCE PRICE**  

     •	CLOSE PRICE > BALANCE PRICE : BUY at balance price high section price
     •	CLOSE PRICE < BALANCE PRICE : SELL at balance price target low section price  

---

## How to Manage Risk

**AOPV (Average Order Book Price Volatility)** is the spread between the two AOP values. Use it to manage risk:

     •	LOW RISK subtract the AOPV spread from your order price (for buy orders) or add it to your order price (for sell orders).
     •	MEDIUM RISK set the stop loss at the sum of the price that directly borders your order price plus your AOPV.
     •	HIGH RISK (For very volatile assets) Set the stop loss at the sum of two price levels above your order price (for sell orders) 
         or two prices levels below your order price (for buy orders) plus AOPV values
---         





