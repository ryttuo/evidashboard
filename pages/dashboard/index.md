---
title: Dashboard
---

<Details title='CVS Dataset'>

  This section is using queries from a .cvs file
  
</Details>

### Airbnb Europe Listings

```sql airbnbs
select * from airbnb_cleanup_europe.airbnb_cleanup_euro where Bedrooms > 2
```

<DataTable data={airbnbs} />


### Listings by City

<!-- <LineChart 
    data={airbnbs}
    x=City
    y=Price 
    yAxisTitle="Prices per City"
    y2SeriesType=bar
/> -->


<Heatmap 
    data={airbnbs} 
    x='Room Type'
    y=City 
    value=Price 
    valueFmt=usd 
/>


<!-- <Histogram
    data={airbnbs}
    x=City
/> -->

<!-- <FunnelChart 
    data={airbnbs} 
    nameCol=Price
    valueCol=City
/> -->