# Trade-Reconciliation
Trade reconciliation project notebook


 What’s the Problem?
 
1. Your Records (Internal Data)
    * You have:
        * Individual monthly trades (March, April, May).
        * One big "quarterly" trade (Q2 = April + May + June).
    * Issue: April and May appear in both your monthly and quarterly trades.
      
2. Clearer’s Records
    * They only show monthly totals (March: 100MWh, April: 500MWh, etc.).
    * They don’t care if you traded monthly or quarterly—they just show the final numbers.
      
What You Need to Do

Step 1: Break Down the Quarterly Trade
* The Q2 trade (300MWh @ €33) covers April, May, June.
* Split it evenly into 3 months:
    * April: 100MWh @ €33
    * May: 100MWh @ €33
    * June: 100MWh @ €33
      
Step 2: Combine Your Trades for Each Month
* For April:
    * You already have a monthly trade (200MWh @ €31).
    * Now add the quarterly part (100MWh @ €33).
    * Total for April:
        * Quantity: 200 + 100 = 300MWh
        * Price: Mix €31 and €33 → €31.67 (weighted average).
* Repeat for May:
    * Monthly: 250MWh @ €32
    * Quarterly: 100MWh @ €33 = 350MWh @ €32.29
* March & June are simpler (no overlap).

  
 Step 3: Compare with Clearer’s Numbers
Month	Your Total	Clearer’s Total	Match?

Mar	100MWh @ €30	100MWh @ €30	✅ Yes
Apr	300MWh @ €31.67	500MWh @ €32	❌ 200MWh missing!
May	350MWh @ €32.29	550MWh @ €32.5	❌ 200MWh missing!
Jun	100MWh @ €33	300MWh @ €33	❌ 200MWh missing!


Step 4: Find the Mismatches
* Your records don’t explain the extra 200MWh the clearer shows for April, May, June.
* Possible reasons:
    * You forgot to record some trades.
    * The quarterly trade was actually larger than 300MWh.
    * The clearer made a mistake (rare, but possible).
