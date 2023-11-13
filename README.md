# Constraints

```python
# Pyspark DataFrame Schema
fifa='''
sofifa_id int NOT NULL,
player_url string NOT NULL,
short_name string NOT NULL,
long_name string NOT NULL,
player_positions string NOT NULL,
overall int NOT NULL,
potential int NOT NULL,
value_eur float,
wage_eur float,
age int NOT NULL,
dob date NOT NULL,
height_cm int NOT NULL,
weight_kg int NOT NULL,
club_team_id int,
club_name string,
league_name string,
league_level int,
club_position string,
club_jersey_number int,
club_loaned_from string,
club_joined date,
club_contract_valid_until int,
nationality_id int NOT NULL,
nationality_name string NOT NULL,
nation_team_id int,
nation_position string,
nation_jersey_number int,
preferred_foot string NOT NULL,
weak_foot int NOT NULL,
skill_moves int NOT NULL,
international_reputation int NOT NULL,
work_rate string,body_type string NOT NULL,
real_face string NOT NULL,
release_clause_eur float,
player_tags string,
player_traits string,
pace int,shooting int,
passing int,dribbling int,
defending int,physic int,
attacking_crossing int NOT NULL,
attacking_finishing int NOT NULL,
attacking_heading_accuracy int NOT NULL,
attacking_short_passing int NOT NULL,
attacking_volleys int NOT NULL,
skill_dribbling int NOT NULL,
skill_curve int NOT NULL,
skill_fk_accuracy int NOT NULL,
skill_long_passing int NOT NULL,
skill_ball_control int NOT NULL,
movement_acceleration int NOT NULL,
movement_sprint_speed int NOT NULL,
movement_agility int NOT NULL,
movement_reactions int NOT NULL,
movement_balance int NOT NULL,
power_shot_power int NOT NULL,
power_jumping int NOT NULL,
power_stamina int NOT NULL,
power_strength int NOT NULL,
power_long_shots int NOT NULL,
mentality_aggression int NOT NULL,
mentality_interceptions int NOT NULL,
mentality_positioning int NOT NULL,
mentality_vision int NOT NULL,
mentality_penalties int NOT NULL,
mentality_composure int,
defending_marking_awareness int NOT NULL,
defending_standing_tackle int NOT NULL,
defending_sliding_tackle int NOT NULL,
goalkeeping_diving int NOT NULL,
goalkeeping_handling int NOT NULL,
goalkeeping_kicking int NOT NULL,
goalkeeping_positioning int NOT NULL,
goalkeeping_reflexes int NOT NULL,
goalkeeping_speed int,
ls string NOT NULL,
st string NOT NULL,
rs string NOT NULL,
lw string NOT NULL,
lf string NOT NULL,
cf string NOT NULL,
rf string NOT NULL,
rw string NOT NULL,
lam string NOT NULL,
cam string NOT NULL,
ram string NOT NULL,
lm string NOT NULL,
lcm string NOT NULL,
cm string NOT NULL,
rcm string NOT NULL,
rm string NOT NULL,
lwb string NOT NULL,
ldm string NOT NULL,
cdm string NOT NULL,
rdm string NOT NULL,
rwb string NOT NULL,
lb string NOT NULL,
lcb string NOT NULL,
cb string NOT NULL,
rcb string NOT NULL,
rb string NOT NULL,
gk string NOT NULL,
player_face_url string NOT NULL,
club_logo_url string,
club_flag_url string,
nation_logo_url string NOT NULL,
nation_flag_url string NOT NULL
'''
```



~~~python
#postgres table schema
'''
sofifa_id INT NOT NULL,
player_url VARCHAR(255) UNIQUE NOT NULL,
short_name VARCHAR(64) NOT NULL,
long_name VARCHAR(255) NOT NULL,
player_positions VARCHAR(64) NOT NULL,
overall INT NOT NULL,
potential INT NOT NULL,
value_eur FLOAT,
wage_eur FLOAT,
age INT NOT NULL,
dob DATE NOT NULL,
height_cm INT NOT NULL,
weight_kg INT NOT NULL,
club_team_id INT, 
club_name VARCHAR(255),
league_name VARCHAR(255),
league_level INT,
club_position VARCHAR(255),
club_jersey_number INT,
club_loaned_from VARCHAR(255),
club_joined DATE,
club_contract_valid_until INT,
nationality_id INT NOT NULL,
nationality_name VARCHAR(255) NOT NULL,
nation_team_id INT,
nation_position VARCHAR(255),
nation_jersey_number INT,
preferred_foot VARCHAR(255) NOT NULL,
weak_foot INT NOT NULL,
skill_moves INT NOT NULL,
international_reputation INT NOT NULL,
work_rate VARCHAR(255) NOT NULL,
body_type VARCHAR(255) NOT NULL,
real_face VARCHAR(255) NOT NULL,
release_clause_eur VARCHAR(255),
player_tags VARCHAR(255),
player_traits VARCHAR(255),
pace INT,
shooting INT,
passing INT,
dribbling INT,
defending INT,
physic INT,
attacking_crossing INT NOT NULL,
attacking_finishing INT NOT NULL,
attacking_heading_accuracy INT NOT NULL,
attacking_short_passing INT NOT NULL,
attacking_volleys INT NOT NULL,
skill_dribbling INT NOT NULL,
skill_curve INT NOT NULL,
skill_fk_accuracy INT NOT NULL,
skill_long_passing INT NOT NULL,
skill_ball_control INT NOT NULL,
movement_acceleration INT NOT NULL,
movement_sprint_speed INT NOT NULL,
movement_agility INT NOT NULL,
movement_reactions INT NOT NULL,
movement_balance INT NOT NULL,
power_shot_power INT NOT NULL,
power_jumping INT NOT NULL,
power_stamina INT NOT NULL,
power_strength INT NOT NULL,
power_long_shots INT NOT NULL,
mentality_aggression INT NOT NULL,
mentality_interceptions INT NOT NULL,
mentality_positioning INT NOT NULL,
mentality_vision INT NOT NULL,
mentality_penalties INT NOT NULL,
mentality_composure VARCHAR(255),
defending_marking_awareness INT NOT NULL,
defending_standing_tackle INT NOT NULL,
defending_sliding_tackle INT NOT NULL,
goalkeeping_diving INT NOT NULL,
goalkeeping_handling INT NOT NULL,
goalkeeping_kicking INT NOT NULL,
goalkeeping_positioning INT NOT NULL,
goalkeeping_reflexes INT NOT NULL,
goalkeeping_speed INT,
ls VARCHAR(32) NOT NULL,
st VARCHAR(32) NOT NULL,
rs VARCHAR(32) NOT NULL,
lw VARCHAR(32) NOT NULL,
lf VARCHAR(32) NOT NULL,
cf VARCHAR(32) NOT NULL,
rf VARCHAR(32) NOT NULL,
rw VARCHAR(32) NOT NULL,
lam VARCHAR(32) NOT NULL,
cam VARCHAR(32) NOT NULL,
ram VARCHAR(32) NOT NULL,
lm VARCHAR(32) NOT NULL,
lcm VARCHAR(32) NOT NULL,
cm VARCHAR(32) NOT NULL,
rcm VARCHAR(32) NOT NULL,
rm VARCHAR(32) NOT NULL,
lwb VARCHAR(32) NOT NULL,
ldm VARCHAR(32) NOT NULL,
cdm VARCHAR(32) NOT NULL,
rdm VARCHAR(32) NOT NULL,
rwb VARCHAR(32) NOT NULL,
lb VARCHAR(32) NOT NULL,
lcb VARCHAR(32) NOT NULL,
cb VARCHAR(32) NOT NULL,
rcb VARCHAR(32) NOT NULL,
rb VARCHAR(32) NOT NULL,
gk VARCHAR(32) NOT NULL,
player_face_url VARCHAR(32) NOT NULL,
club_logo_url VARCHAR(255),
club_flag_url VARCHAR(255),
nation_logo_url VARCHAR(255),
nation_flag_url VARCHAR(32) NOT NULL,
year INT NOT NULL
PRIMARY KEY (year,sofifa_id)
'''
~~~



# Description

1. `sofifa_id`: Unique ID for a player in the SOFIFA database.
2. `player_url`: URL linking to detailed information about the player.
3. `short_name`: Shortened version of the player's name.
4. `long_name`: Full name of the player.
5. `player_positions`: Positions that the player can play.
6. `overall`: Overall rating of the player's skills.
7. `potential`: Potential future rating of the player.
8. `value_eur`: Monetary value of the player in Euros.
9. `wage_eur`: Player's weekly wage in Euros.
10. `age`: Age of the player.
11. `dob`: Date of birth of the player.
12. `height_cm`: Height of the player in centimeters.
13. `weight_kg`: Weight of the player in kilograms.
14. `club_team_id`: ID for the club team the player belongs to.
15. `club_name`: Name of the player's club team.
16. `league_name`: Name of the league the player's club participates in.
17. `league_level`: Level of the league.
18. `club_position`: Position of the player within the club.
19. `club_jersey_number`: Jersey number of the player in the club.
20. `club_loaned_from`: If applicable, the club from which the player is loaned.
21. `club_joined`: Date when the player joined the current club.
22. `club_contract_valid_until`: Validity date of the player's contract with the club.
23. `nationality_id`: ID for the player's nationality.
24. `nationality_name`: Name of the player's nationality.
25. `nation_team_id`: ID for the player's national team.
26. `nation_position`: Position of the player within the national team.
27. `nation_jersey_number`: Jersey number of the player in the national team.
28. `preferred_foot`: Preferred foot of the player.
29. `weak_foot`: Rating of the player's weaker foot.
30. `skill_moves`: Rating of the player's skill moves.
31. `international_reputation`: Player's reputation in international competitions.
32. `work_rate`: Work rate of the player.
33. `body_type`: Body type of the player.
34. `real_face`: Indicates if the player's face is realistically represented.
35. `release_clause_eur`: Monetary release clause in Euros.
36. `player_tags`: Tags associated with the player.
37. `player_traits`: Special traits associated with the player.

38-66. Various attributes related to the player's skills, movement, power, mentality, defending, and goalkeeping.

67-101. Overall and potential rating of the player in different positions.

102-109. URLs for player images, club logo, club flag, nation logo, and nation flag.

# Comments on the regressors and the impact of tunable parameters
GBT： The expressive power of Gradient Boosted Trees (GBT) is notable. And it can an capture complex non-linear relationships in the data. This makes it effective in scenarios where the relationship between input features and the target variable is not linear.     
We choose to tune maxDepth and maxIter.      
By tuning maxDepth, we can control overfitting and improve computational efficiency, because high maxDepth might cause overfitting and result in expensive time cost. By tuninbg maxIter, we can avoid underfitting and control trianing time, because low maxIter might result in underfitting the data.      

Linear Regression: Training and making predictions with linear regression models are computationally efficient, especially when dealing with large datasets. What's more, it can serve as an benchmark of regression problem.     
We choose to tune regParam and maxIter in Linear Regression.    
By tuning regParam, we can control the degree of regularization, which deals with a trade-off between the bias and variance of the model. By tuning maxIter, we can make a trade-off between speed and convergence.    
