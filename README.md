# Financial Report


## Project Overview 

## Data Sources 
- excel 

## Data Cleaning

Data table created through query editor
Many to One relationship between data and fincial table 

## Data Analysis 

### Total Sales
```dax
Total Sales = SUM(financials[ Sales])
```
### Total Cost of Goods Sold
```dax
Total COGS = sum(financials[COGS])
```
### Total Margin
```dax
Total Margin = sum(financials[profit])
```
### Profit Percentage
```dax
Profit % = [Total Margin] / [Total COGS]
```

```dax
Measure Selected = SELECTEDVALUE(Metrics[Measure], "Total Sales"
```

```dax
Measure Logic = Switch(true(),
'All Measures' [Measure Selected] ="Total Sales", [Total Sales],
'All Measures' [Measure Selected] ="Total COGS", [Total COGS],
'All Measures' [Measure Selected] ="Total Profit", [Total Margin],
[Total Sales])
```
## Findings 

## Recommendations 

## Limitations

