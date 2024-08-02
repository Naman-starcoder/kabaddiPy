---
title: Player Functions
layout: default
has_toc: true
has_children: false
---
## Table of Contents
  - [get\_stats\_from\_player\_profile](#get_stats_from_player_profile)
  - [player\_performance](#player_performance)
  - [get\_all\_player\_team\_url](#get_all_player_team_url)
  - [get\_players\_team\_info\_and\_profile\_url](#get_players_team_info_and_profile_url)



## get_stats_from_player_profile

Retrieves statistics from a player's profile page.

### Usage

```python
aggregator = KabaddiDataAggregator()
player_stats = aggregator.get_stats_from_player_profile(profile_name)
```

### Parameters

- `profile_name` (str): The player's name.

### Returns

- `Dict[str, str]`: A dictionary containing:
  - Two key-value pairs for player statistics (keys and values depend on the available data)
  - `teamName`: The name of the player's team

---



## player_performance

Retrieves player performance data from all seasons or particular seasons.

### Usage

```python
aggregator = KabaddiDataAggregator()
player_performance_data = aggregator.player_performance()
```
### Returns

- `List`: A list containing player performance data extracted from the Tableau dashboard. The structure depends on the data available in the dashboard.

---
## get_all_player_team_url

**Internal function**. Retrieves the URLs for all player team pages on the Pro Kabaddi website.

### Usage

```python
aggregator = KabaddiDataAggregator()
player_team_urls = aggregator.get_all_player_team_url()
```

### Returns

- `List[str]`: A list of URLs for player team pages.

---
## get_players_team_info_and_profile_url

**Internal function**. Retrieves information about players, including their names, profile URLs, and team URLs.

### Usage

```python
aggregator = KabaddiDataAggregator()
players_info = aggregator.get_players_team_info_and_profile_url()
```

### Returns

- `List[Dict[str, str]]`: A list of dictionaries, each containing:
  - `name`: Player's name
  - `profileURL`: URL of the player's profile page
  - `teamURL`: URL of the player's team page

---



<<<<<<< HEAD
=======

## player_performance

Retrieves player performance data from a Tableau dashboard.

### Usage

```python
aggregator = KabaddiDataAggregator()
player_performance_data = aggregator.player_performance()
```

### Returns

- `List`: A list containing player performance data extracted from the Tableau dashboard. The structure depends on the data available in the dashboard.
  
---

**Note**: The functions that interact with constantly updating dashboards (`team_line_up`, `team_level_stats`, and `player_performance`) may return complex data structures. The exact format of the returned data depends on the structure and content of the Tableau dashboards at the time of extraction.