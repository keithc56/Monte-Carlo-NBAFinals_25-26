# NBA Playoff Monte Carlo Simulator — Spurs vs. Knicks

This simulation was created with the intent to run a Monte Carlo 
simulation using the Spurs and Knicks playoff offensive and defensive 
ratings, their opponents offensive and defensive ratings, and the 
offensive and defensive ratings of both teams when they played head 
to head over the course of the last 3 seasons. The intention was to 
see how accurate a Monte Carlo simulation could be and develop an 
applicable scatter plot showing all 1,000 simulations.

## Methodology

Ratings are adjusted using a playoff strength-of-schedule (SOS) 
modifier derived from the difference between each team's average 
opponent ratings and the league average. Variance is calculated from 
3 seasons of head-to-head game logs using NumPy standard deviation, 
then blended across both offensive and defensive dimensions.

## Results

Within this Monte Carlo simulation, the Knicks are barely favorites 
and are only a 4 point favorite at max. With no adjustment for home 
court situations or injuries, I highly anticipate this series to go 
to either 6 or 7 games. I will be backtracking this data as the 
series progresses.

According to further research, when the odds are this close there is 
an 86.9% chance the series goes to at least 5 games before a winner 
is decided.

## Known Limitations

There may be an error in logic simply due to the fact that the Knicks 
and Spurs who played 2-3 seasons ago are not the same Knicks and Spurs 
this year. However, many of the key players remain the same, which is 
why head-to-head history was still used as the variance input rather 
than discarded entirely.

No adjustments were made for:
- Home court advantage
- Player injuries
- Playoff fatigue or rest days

## Skills Demonstrated
- Monte Carlo simulation design
- Strength-of-schedule adjustment methodology
- Statistical variance modeling (NumPy)
- Data visualization (Matplotlib scatterplot)
- Analytical backtracking against real outcomes

## How to Run
pip install -r requirements.txt
python simulator.py

**Backtracking**
## Game 1 — Knicks 105, Spurs 95
**Series: Knicks lead 1-0**

The simulation correctly predicted the Knicks to win Game 1, though 
the actual margin of +10 was more decisive than the predicted +2.4. 
The game total of 200 came in well under the simulated over/under of 
217.9, suggesting both defenses outperformed expectations. 
However the score still falls within our Monte Carlo simulation
so I consider it the model a success for Game 1 as the favorites
won and the margin was within our Monte Carlo simulation.

**Knicks standouts:** Jalen Brunson led all scorers with 30 points on 
12-31 shooting. Karl-Anthony Towns added 18 points and 12 rebounds. 
Josh Hart contributed a massive +22 in just 27 minutes with 15 
rebounds despite only scoring 3 points.

**Spurs standouts:** Victor Wembanyama posted 26 points and 12 rebounds 
but fouled out with 6 fouls in 38 minutes. Dylan Harper showed well 
off the bench with 16 points. De'Aaron Fox struggled shooting 3-13 
from the field.

**Key observation:** Wembanyama fouling out is a variable the simulation 
could not account for and likely contributed to the margin being wider 
than predicted. This supports the known limitation around injury and 
foul trouble adjustments.

### Game 2 — Knicks 105, Spurs 104
**Series: Knicks lead 2-0**

Game 2 is the strongest validation of the model so far. A 1 point 
margin is nearly identical to the predicted +2.4, confirming that 
the simulation's core methodology is sound. The game total of 209 
also trended closer to the predicted 217.9 than Game 1.

**Knicks standouts:** Karl-Anthony Towns posted 21 points and 13 
rebounds. Mikal Bridges and Jalen Brunson each scored 20, though 
Brunson shot 7-25 from the field. Landry Shamet came off the bench 
with 13 points on 5-12 shooting at +9.

**Spurs standouts:** Victor Wembanyama was dominant with 29 points, 
9 rebounds, 2 steals, and 4 blocks on 11-21 shooting, staying out 
of foul trouble this time, However he committed key errors at the 
end of the game turning the ball over while the game was tied with 
9 seconds left and committing a foul on Jalen Brunson.
De'Aaron Fox bounced back with 20 points 
on 8-12 shooting. Dylan Harper continued his strong series with 15 
points and a +12 rating off the bench.

**Key observation:** Game 2 was played in San Antonio with no home 
court adjustment in the model, yet the Knicks still won by 1.
Wembanyama playing a full 40 minutes without foul 
trouble and the Spurs still losing by 1 on their home floor is a 
notable data point — the model's predicted margin held almost exactly.

### Game 3 — Spurs 115, Knicks 111
**Series: Knicks lead 2-1**

The first Knicks loss of the series and the first result that fell 
on the Spurs side of the simulation. The actual total of 226 came 
in over the predicted 217.9, the first over of the series. Notably 
this is the first game played at Madison Square Garden, a home court 
variable the model does not account for — yet the Spurs won on the 
road, which is a meaningful data point.

**Spurs standouts:** Victor Wembanyama was exceptional with 32 points, 
8 rebounds, 6 assists, 2 steals, and 3 blocks on 11-18 shooting. 
Stephon Castle added 23 points on 8-14 shooting. Devin Vassell 
contributed 11 points shooting a near perfect 3-4 from three. Julian 
Champagnie added 12 off the bench.

**Knicks standouts:** OG Anunoby led New York with 28 points on 9-13 
shooting. Jalen Brunson scored 32 but on an inefficient 11-25 from 
the field with 5 turnovers. Josh Hart added 16 points and 9 rebounds
which is a stark contrast to his game 2 statline of 0 points and 
6 rebounds.

**Key observation:** Wembanyama posted his best game of the series 
with a full stat line — 32 points, 8 rebounds, 6 assists, and 3 
blocks. When he plays at this level without foul trouble the model's 
Knicks-favored prediction is clearly challenged. Landry Shamet's -20 
in 23 minutes was a significant liability for New York. The series 
competitiveness through 3 games continues to support the original 
86.9% projection for a 5+ game series.

## Skills Demonstrated
- Monte Carlo simulation design
- Strength-of-schedule adjustment methodology
- Statistical variance modeling (NumPy)
- Data visualization (Matplotlib scatterplot)
- Analytical backtracking against real outcomes

## Personal Note

I hope my Monte Carlo simulation proves accurate — however, I also 
hope the odds tip in the Spurs' favor.
