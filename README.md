# Pure Sip Beverages: Automated Sales Reporting Dashboard
**Tools:** Power BI, Power Query (M)
**Data:** Sales spreadsheets from four retailers (Walmart, Costco, Walgreens and Target) across three states, covering six beverage brands: about $1.21M in sales and 2.3M units.

## Business overview
Pure Sip Beverages distributes popular beverage brands such as Coca-Cola, Sprite and Fanta, and supplies major retail chains including Costco, Walgreens, Target and Walmart.

## The business problem
Pure Sip tracked sales in separate spreadsheets maintained by each regional manager. This siloed approach caused three problems:
1. **Data consolidation:** combining the spreadsheets for regional reporting was slow, manual and error-prone.
2. **Data accuracy:** inconsistent formats and data entry practices across locations led to inaccurate reporting.
3. **Limited analysis:** spreadsheets offered little support for advanced analysis and visualisation, so the company lacked clear insight into sales trends and performance across locations.

## My solution
I built a Power BI report that connects to a shared folder of sales files, so the data is consolidated and cleaned in one place:
1. **Centralised data collection:** each retailer's quarterly sales spreadsheet is saved to a shared folder.
2. **Automated cleaning and consolidation:** Power BI connects to the folder and combines every file into one dataset, applying the same cleaning steps to each file.
3. **Simple updates:** when a new file is added to the folder and the report is refreshed, it is included automatically, with no manual copying or re-cleaning.

## My role and approach
1. **Connected to the folder:** used Get Data → Folder in Power BI to load all the sales files together and combined them into a single table.
2. **Cleaned the data in Power Query:** Because the steps run on every file, new files are cleaned in the same way.
3. **Built the report measures:** Total Sales, Total Quantity Sold, Number of Retailers, Number of States and a sales-versus-target KPI (target: $250,000).
4. **Designed the dashboard:** a one-page report with a KPI tracker, a monthly sales trend, a regional map, and retailer and brand comparisons, with slicers for Beverage Brand and Contact.


## What the dashboard shows
- Sales performance against target
- How sales change from month to month
- Which regions, retailers and brands generate the most sales

## Key findings
- **Headline numbers:** $1,213,018 in total sales and 2,309,850 units sold, across 4 retailers and 3 states.
- **Target:** the KPI tracker shows $238,850 against a target of $250,000, which is $11,150 (4%) below target. 
- **Seasonality:** sales are lowest in February ($78.6K), rise steadily to a peak in August ($116.0K), dip in September and October, then recover to $115.3K in December. The second half of the year (about $670K) is roughly 23% higher than the first half (about $543K).
- **Retailers:** Walmart leads with $392K (32% of sales), then Costco ($332K, 27%), Walgreens ($251K, 21%) and Target ($239K, 20%). Walmart and Costco together account for about 60% of sales.
- **Brands:** Dasani Water is the top brand ($234K, 19%), followed by Coca-Cola ($228K), Diet Coke ($214K), Sprite ($189K), Powerade ($181K) and Fanta ($167K, 14%). The top three brands make up just over 55% of sales.
- **Regions:** sales come from California, Texas and New York. The map shading suggests California is the strongest with total sales of $582,400 and Texas the weakest with total sales $238,850. 

## Recommendations
1. **Protect the two anchor retailers while broadening the base.** Walmart and Costco generate about 60% of sales, which makes Pure Sip dependent on them. Grow Walgreens and Target with retailer-specific promotions and shelf-space deals.
2. **Plan stock and promotions around seasonality.** Build inventory and staffing ahead of the May to August ramp-up, and test promotions in February and in September to October to smooth the dips.
3. **Review the weaker brands.** Fanta and Powerade trail the leaders. Check whether the gap comes from distribution, shelf space or pricing at particular retailers before investing in promotions.
4. **Build on Dasani Water.** As the top brand, it is a good candidate for cross-promotion alongside the Coca-Cola, Diet Coke and Sprite products.
5. **Track performance against target month by month.** Sales are 4% below target, so reporting the gap by retailer and brand would show where to act first.
6. **Consider expanding into more states.** Sales come from only three states, so there may be room to grow if other regions fit Pure Sip's distribution capacity.
7. **Standardise the file template.** Give every retailer the same spreadsheet layout and required columns, so new files load cleanly and the automation doesn't break. Consider monthly uploads instead of quarterly ones for fresher reporting.

## What I learned
This project taught me to build a reusable data pipeline in Power BI, where a folder connection and Power Query steps replace repeated manual consolidation, and to turn the result into a dashboard that answers business questions quickly.

## Repository contents
- README.md: this write-up
- dashboard/: screenshots of the dashboard and the Power Query steps
- powerbi/: the Power BI (.pbix) file
