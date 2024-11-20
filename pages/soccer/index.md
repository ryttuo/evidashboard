---
title: Soccer
---

<Details title='Sqlite Dataset'>

  This section is using queries from sqlite
  
</Details>

### Teams

```sql teams
select * from european_soccer.teams
```

<DataTable data={teams} />


### Players
##### Overall rating > 80

```sql players_data
select * from european_soccer.players
```

```sql attacking_work_rates
select attacking_work_rate from european_soccer.players
where attacking_work_rate != 'le' and attacking_work_rate != 'norm'
```

###### Players Attack
<Dropdown data={attacking_work_rates} name=attacking_work_rate value=attacking_work_rate>
    <DropdownOption value="%" valueLabel="All"/>
</Dropdown>


```sql data_attacking_work_rate
select  
    attacking_work_rate,
    height as height,
    acceleration,
from european_soccer.players
where attacking_work_rate like '${inputs.attacking_work_rate.value}'
and attacking_work_rate != 'le' and attacking_work_rate != 'norm' 
and attacking_work_rate != 'y' and attacking_work_rate != 'stoc' 
group by all
order by acceleration desc
```

<BarChart
    data={data_attacking_work_rate}
    title="Players acceleration and Height by {inputs.attacking_work_rate.label} attack"
    x=height
    y=acceleration
    series=attacking_work_rate
/>


```sql team_attributes
select * from european_soccer.team_attributes
```

```sql player_attributes
select * from european_soccer.player_attributes
```

### Leagues

```sql leagues
select name from european_soccer.leagues
```

<DataTable data={leagues} />