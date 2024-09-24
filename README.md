**VENDOR QUALITY PERFROMANCE - FURNITURE RETAIL**
The Power BI report will let you know which vendor is performing better in terms of rejections and reworks on their manufactured furnitures.
The report contains:

**CARDS**

**HEAT MAP AS CALENDER**

**SLICERS**

**DONUT CHART**

**LINE AND STACKED COLUMN**

**TABLE**

**BOOKMARKS**

**DRILLTHROUGH FEATURES**

**DRILL DOWN**

**RESET BUTTON**


**MEASURES USED:**

1. **Contri** - contri = DIVIDE(SUM('MTO Sofas'[Qtys. offered for inspection]),[Total offered for contri purpose])

2. **Countvend** - Countvend = CALCULATE(DISTINCTCOUNT('MTO Sofas'[Vendor name]),ALL('MTO Sofas'[Vendor name]))

3. **Most rejected model** - Most rejected model = TOPN(1,ALL('MTO Sofas'[Sofa Model]),[Total rejected],DESC)

4. **Most rejeced model in terms of rej rate** - Most rejected model in terms of rej.rate = IF([Rate of Rejection],SELECTCOLUMNS('MTO Sofas','MTO Sofas'[Sofa Model]),"No Rejections")

5. **RankR** - RankR = RANKX(ALL('MTO Sofas'[Vendor name]),[Rate of Rework], ,ASC,Skip)

6. **Rank** - Rank = RANKX(ALL('MTO Sofas'[Sofa Model]),[Rate of Rejection], ,ASC,Dense)

7. **Rate of Rejection** - Rate of Rejection = DIVIDE([Total rejected],[Total Offered])

8. **Rate of Rework** - Rate of Rework = DIVIDE([Total rework],[Total Offered])

9. **SKUCOUNT** - SKUCOUNT = DISTINCTCOUNTNOBLANK('MTO Sofas'[SKU])

10. **Total offered** - Total Offered = SUM('MTO Sofas'[Qtys. offered for inspection])

11. **Total Offered for contri purpose** - Total offered for contri purpose = CALCULATE(SUM('MTO Sofas'[Qtys. offered for inspection]),ALL('MTO Sofas'))

    
**SHOWN BELOW A SCREENSHOT OF THE REPORT BUILT IN POWER BI**

![image](https://github.com/user-attachments/assets/848b337a-b541-4889-aba3-dfdaf49e222e)
