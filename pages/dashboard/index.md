---
title: Dashboard with cvs
---

### Airbnb Europe Listings

```sql airbnbs
select * from airbnb_cleanup_europe.airbnb_cleanup_euro
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
    x=Day 
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