# Promiedos Scrapper

## Methods of the main object:

### Get Matches

get_matches(league, round(default last), json(default false))

return an array(if json = false) with the form ["date", "hour", "team", "team" ...]
it is not convinient to use this form because you will have to separate the date and hour manually

example:
get_matches("espana", 3)
return:
['Viernes 30 de Agosto', '15:00 ', 'Sevilla', 'Celta de Vigo', '17:00 ', 'Athletic Bilbao', 'Real Sociedad', ' Sabado 31 de Agosto', '12:00 ', 'Osasuna', 'Barcelona', '14:00 ', 'Getafe', 'Alaves', '14:00 ', 'Levante', 'Valladolid', '16:00 ', 'Betis', 'Leganes', ' Domingo 1 de Septiembre', '12:00 ', 'Valencia', 'Mallorca', '14:00 ', 'Atletico Madrid', 'Eibar', '14:00 ', 'Espanyol', 'Granada', '16:00 ', 'Villarreal', 'Real Madrid']

get_matches("espana", 3, json=true):

to do

### Get Scores

get_scores(league, round, json(default false))

Same usage as get matches

return an array(if json = false) with the form ["home team", "goals scored by home", "goals scored by away", "away team" ...]
(if the match does not started, it not return anything between the two teams)

example:
to do

### get_standings

get_standings(league, team=False, json=False)

return an array of strings, every string with the form:
team points matches played w d l goals scored goals conceded goal difference

if json == true it return a json with the form
'team': {'pos': 0, 'GF': 0, 'GD': 0, 'losses': 0, 'draws': 0, 'wins': 0, 'played': 0, 'points': 0, 'GA': 0}}