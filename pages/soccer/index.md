---
title: Soccer
---

### Teams

```sql teams
select * from european_soccer.teams
```

<DataTable data={teams} />


### Players

```sql players
select * from european_soccer.players
```

## Attri


<!-- <DataTable data={players} /> -->
<!-- 
<Dropdown data={players} name=player value=player>
    <DropdownOption value="%" valueLabel="All Players"/>
</Dropdown> -->


### Team Attributes

```sql team_attributes
select * from european_soccer.team_attributes
```

<!-- <DataTable data={team_attributes} /> -->


### Player Attributes

```sql player_attributes
select * from european_soccer.player_attributes
```

<!-- <DataTable data={player_attributes} /> -->


### Leagues

```sql leagues
select * from european_soccer.leagues
```

<!-- <DataTable data={leagues} /> -->