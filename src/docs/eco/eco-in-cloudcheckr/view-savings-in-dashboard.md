<meta name="robots" content="noindex">

# View Savings in Dashboard

Once Eco has been enabled for your organization the Eco dashboard will show a complete view of your savings.

## Filters

The default view of the dashboard shows data from all the accounts in your organization.

By default, the dashboard shows data since the first day of your AWS account, from all regions, and from all of your AWS services. However, you can use the drop-down filters to limit the scope of data displayed. For example, you can display according to services such as EC2, RDS, and ElastiCache.

You can set the following filters:

- Time: Choose the range of dates for which data will be displayed.
- Regions: Choose the regions which will be included in the charts and tables.
- Selected Services: Choose the services which will be included in the charts and tables.

## Summary Line

The Overview dashboard includes a summary line which displays the following information:

- Total Saved: Total amount saved as a result of reserved instance utilization.
- Current Commitment:The amount currently committed to reserved instances. The lower the commitment, the more flexible and dynamic the account's compute resources can be.
- Additional Potential Savings: The amount of additional potential savings in USD on top of existing RIs.
- Current EC2 Commitment: The current percentage of On-Demand instances in the account that are covered by reservations.
- Max EC2 Commitment: Maximum potential committed amount.

## Graphs and Charts

Eco provides summary graphs and charts to give you wide visibility of your savings and commitments. The graphs and charts can be filtered according to the items in the legend. The following graphs are displayed:

### Savings over time

A bar graph showing the amount of savings each month broken down by type of savings. This graph will allow you to visualize savings from reservations and savings plans. You can use the filters at the top of the page and source filters specific to each graph.

- All: This source filter displays all savings provided by Eco, Non-Eco and Support Savings.
- Eco: This source filter displays all savings provide by Eco.
- Non-Eco: This source filter displays all savings provided by the customer. 
- Support Savings: This source filter displays all savings Eco saved you on AWS Support Plans. AWS provides different Support Tiers and charges differently for each tier. Spot retrieves and calculates how much a customer would be spending on support if they weren’t using Eco. Eco does not charge customers based on these savings.

<img src="/eco/_media/tutorials-view-savings-1.png" />

### Monthly Commitment over Time

A stacked bar graph showing your reserved instance and savings plan commitment per month broken down into Standard, Convertible, and Pending reservations, plus Compute and EC2 savings plans. Use the toggle switches to include or exclude recurring fees or show up-front fees from an amortized view.

<img src="/eco/_media/tutorials-view-savings-01c3a.png" />

The export from this table provides an amortization report, which breaks down each commitment as a CSV file with the following headers.

- Amortized Commitment: The amortized amount for the month. If there was no upfront commitment, this will be zero.
- ARN: The AWS Resource Name unique to the commitment.
- Date: The year and month of the amortized amount.
- Duration: The number of seconds used in the calculation for which the investment should provide discounts with consideration for RI marketplace transactions.
- Expiration: The expiration date of the commitment.
- Instance Family or Type: The instance family of the reservation or type of the savings plan.
- Region: The region in which the commitment was purchased.
- Upfront Commitment: The basis for the amortized commitment. If there was no upfront commitment, this will be zero.

### Coverage over Time

A line graph that breaks down the story of how reservations, savings plan coverage, and commitments relate to your overall savings. The left chart is the simplest, showing the difference between your actual spend and what could have been your costs for reservable services without a savings strategy. On the right, you see the same data, but with your actual spend explained as the combination of commitment cost and uncovered spend. The coverage calculation considers dollars or your investment used instead of hours, which is different from AWS cost explorer. For actual spend, the calculation only considers what is reservable for a service (e.g., Eco only uses the on-demand purchase option, with the Running Hours usage type groups and the Usage charge type).

<img src="/eco/_media/tutorials-view-savings-01d.png" />

### Commitment Usage Distribution Over Time

A filterable table and corresponding chart which allow you to review your commitments in a variety of ways. By placing your cursor in the filter field, you will see which parameters can be selected.

<img src="/eco/_media/tutorials-view-savings-01e2.png" />

- Account ID: Account number identifier.
- Commitment ID: Identifier of the Reservation or Savings Plan. The row and ID appear when it fits within the relevant filters.
- Commitment Type: Standard RI, Convertible RI, Compute Savings Plan, or EC2 Savings Plan.
- $ Used: The total equivalent cost within the time range multiplied by the utilization.
  - Example 1: If the time range covered the entire term of the reservation, it was 100% utilized, and the total equivalent cost was $1000, the result would be $1000.
  - Example 2: If the time range was half the history of the same reservation, it would be $500.
  - Example 3: If it was only 50% utilized during that period, it would be $250.
  - Example 4: If the term of the RI is three years and only one year of the period has passed since it was purchased, it would be possible to show only 33.3% of the total equivalent cost in this field, at maximum.
- % Used: Utilization within that time period.
- Equivalent OD Price: What the on-demand price would have been during that time period.
- Generated Savings: How much you saved due to using commitments' discounted rates instead of the full on demand rates. Calculation: On Demand equivalent minus commitments minus uncovered spend. Not necessarily the same as net savings.
- Source: Eco or Non-Eco.

### Total Active Commitments

This chart provides amortized costs (i.e., up-front plus recurring costs) of all active commitments according to the designated filters and views.

<img src="/eco/_media/tutorials-view-savings-02a.png" />

## Commitment Details Report

Below the overview graphs and pie charts, you can see a table with detailed information about your reserved instances, including your total generated savings at the bottom of the table.

<img src="/eco/_media/tutorials-view-savings-02.png" />

### Filter Data

You can filter the data displayed according to several criteria available.

1. Place your cursor in the filter and click a parameter.

<img src="/eco/_media/tutorials-view-savings-03.png" width="242" height="219" />

2. Choose the specific value(s) to be displayed by typing them or selecting from the list.

<img src="/eco/_media/tutorials-view-savings-04.png" width="244" height="223" />

### Display Columns

You can customize the columns that appear in the table. The following column headings are available:

- Savings type:
  - COMP SP: Compute Savings Plan
  - EC2 SP: EC2 Savings Plan
  - SAGE SP: Sagemaker Savings Plan
  - RI-S: Standard Reserved Instance
  - RI-C: Convertible Reserved Instance
- Instance type
- Quantity: The number of instances in the batch.
- Service
- Region
- OS
- Payment option: Indicates how you have opted to pay for the RIs: All upfront, partial upfront, or no upfront payment.
- Offering class: Indicates whether the RIs are standard or convertible.
- Start date: The date on which this batch of RIs was purchased.
- End date: The date on which this purchase commitment will end.
- OD cost equivalent: The amount it would cost to use the same resources with on-demand instances.
- Generated savings: The amount the commitment saved over using strictly on-demand instances.
- Source: Indicates whether the RIs were purchased by Eco or not.
- Generated savings: Savings generated due to the use of reservations.
- ARN: The unique AWS ID for each reservation. This column is available only when you export data.

### Export Data

To export the Reservation Details report to a CSV file, click Export above the table. The exported data will include the ARN for each reservation.

## What's Next?

Learn more about the [Eco AWS policy](eco/tutorials/eco-policy/).
