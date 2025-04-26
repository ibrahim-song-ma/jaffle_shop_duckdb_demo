## normal metrics
```bash
mf list dimensions --metrics order_total
mf list entities --metrics order_total
mf query --metrics order_total,orders --group-by order_id__is_food_order,metric_time --limit 10 --order -metric_time --where "order_id__is_food_order = True" --start-time '2016-09-01' --end-time '2017-08-31'
mf query --metrics order_total,orders --group-by order_id__is_food_order,metric_time__month --limit 10 --order -metric_time__month --where "or der_id__is_food_order = True" --start-time '2016-09-01' --end-time '2017-08-31'
```

## cumulative metrics
```bash
mf list dimensions --metrics cumulative_revenue_mtd
mf query --metrics cumulative_revenue_mtd --group-by metric_time --order metric_time --start-time '2016-09-01' --end-time '2017-08-31' 
mf query --metrics cumulative_revenue_mtd --group-by metric_time__month --order metric_time__month --start-time '2016-09-01' --end-time '2017-08-31'
mf query --metrics cumulative_revenue_l1m --group-by metric_time --order metric_time --limit 40 --start-time '2016-09-01' --end-time '2017-08-31' 
```

## Derived metrics
```bash
mf list dimensions --metrics revenue_growth_mom
mf query --metrics revenue_growth_mom --group-by metric_time --order metric_time --start-time '2016-09-01' --end-time '2017-08-31'
mf query --metrics revenue_growth_mom --group-by metric_time__month --order metric_time__month --start-time '2016-09-01' --end-time '2017-08-31' 
```

##Ratio
```bash
mf query --metrics food_revenue_pct --group-by metric_time__month --order metric_time__month --start-time '2016-09-01' --end-time '2017-08-31'
```