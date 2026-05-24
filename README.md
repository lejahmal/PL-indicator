<img width="1112" height="747" alt="PL tutorial" src="https://github.com/user-attachments/assets/0b964f0e-f77f-47c4-b3d7-087a7fd10106" />

AFTER COMPLETED FILTERS FROM STEP 1 TO STEP 9 

      •	For automatic process go to DISPLAY > MACROS > MATRICE > Execute the matrice will loop LINE 2 PARAMS up to MAKER will be equal to 
        PIVOT (step 5 value is the pivot name in the standard case pivot is always O+ but another matrice point can be used as PIVOT in 
        advanced study case ) the ERROR MARGIN is the  spread between MARKER and PIVOT when it is zero step 7  will show STATIC  

        For manual process manually change the value of LINE 2 PARAMS and verify if MARKER equal PIVOT and step 7 show STATIC when 
        completed start read orderbook price (for manual process ERROR MARGIN around 0.01 is accepted)

      •	# Move the $ symbol cursor price along the vertical line to the price closest to the asset's current price on the date of the 
         study.


READ PREDICTED ORDERBOOK THIS WAY

      ORDERBOOK is divided in three sections
      •	Section 1 between Go price and AOP3 
      •	Section 2 between AOP3 and AOP4 
      •	Section 3 between AOP4 and corresponding price

      Every section contains two ranges price 
      •	Section range itself 
      •	Tension range (intra section part between the RED PRICE color around BALANCE PRICE and BORDER PRICE) 

      Every AOP have two price 
      •	The more great is the average price to use in case of sell 
      •	The less great is the average price to use in case of buy

HOW TO OPEN TRADE

      •	CURSOR PRICE IN SECTION 1
        After place cursor price, find the tension range and check if asset is ranging at least one time in the tension range if true use 
        red price  or border price as next order entrance in the following trend if not enter at volatility price that means price is 
        going to ranging section itself

      •	CURSOR PRICE IN SECTION 2
        Check whatever price as ranged at least one time in tension range if true use red price  or border price as next order entrance 
        in the following trend if not use the lower AOP to buy in the following trend or higher AOP to sell in the following trend 

      •	CURSOR PRICE IN SECTION 3
        Check whatever price as ranged at least one time in tension range if true use red price  or border price as next order entrance 
         in the following trend if not use the lower AOP to buy and target next AOP4 higher in the following trend or higher AOP to sell 
         target VOLATILITY PRICE in the following trend 


HOW TO MANAGE RISK 
      AOPV (Average orderbook price volatility) who is the spread between the two AOP values
      STOP LOSS to mage risk in efficient way while using predicted orderbook can be done in 3 way 
      •    If you want to take the less risky remove AOPV spread to order price in case of buy or add or to order price in case of sell 
      •    If you want to take an average risk SL with the sum of price that directly border your order price plus your AOPV
      •    If you want to take the high risk in case of very volatile asset, SL with the sum of two price upper your order price in case 
           of sell or two level price lower plus AOPV
