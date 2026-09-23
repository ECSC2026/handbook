## 7.1. Jeopardy Scoring

The Jeopardy competition will use dynamic scoring. Each challenge is worth 1000 points at the beginning of the competition, regardless of category or difficulty. A challenge's value decreases to 100 points as more teams solve the challenge, according to the following formula:


$$
\mathsf{score} = \left\lceil \mathsf{maximum\_points} \cdot \left( \frac{\mathsf{minimum\_points}}{\mathsf{maximum\_points}} \right)^{\left(\left(\frac{\mathsf{max}(0, \mathsf{\# solves}-1)}{\mathsf{max}(1, \mathsf{\# teams}-1)}\right)^\alpha\right)} \right\rceil
$$


Here,

$$
\mathsf{maximum\_points} = 1000\newline\mathsf{minimum\_points} = 100\newline \alpha = 0.705
$$

so the final formula is as given by the following Python function:

```python
def score(solves: int, teams: int, minimum_points: int = 100, maximum_points: int = 1000, alpha: float = 0.705):
    decay = (max(0, solves - 1) / max(1, teams - 1)) ** alpha
    return math.ceil(maximum_points * (minimum_points / maximum_points) ** decay)
```


The total number of points of each team is the sum of the points across all challenges solved by that team at the end of the competition. Specifically, it is *not* the sum of points the challenge had at the time of the solve. Each team receives exactly the same amount of points for a given challenge.

Example point values with 42 participating teams:

| Challenge solve count | Points |
|-----------------------|--------|
| 0                     | 1000   |
| 1                     | 1000   |
| 2                     | 846    |
| 5                     | 640    |
| 10                    | 454    |
| 15                    | 340    |
| 25                    | 207    |
| 35                    | 133    |
| 40                    | 109    |
| 42                    | 100    |


"First bloods" (the first solve of a challenge) will be recognized and celebrated, but will not award additional points beyond eternal glory.

## 7.2. Attack-Defense Scoring

For the Attack-Defense scoring formula, please refer to the Attack-Defense wiki at <https://wiki.ad.ecsc2026.de/scoring/>

## 7.3. Aggregated Scoring

The aggregated scoring is computed by combining teams' scores on the two competition days as described by the following formula. For each team:

```
aggregated_score = jeopardy_score + ad_normalized_score
```

where `jeopardy_score` is the team's score at the end of the jeopardy competition and`ad_normalized_score` is the team's score at the end of the attack/defense competition, normalized on the same scale as the jeopardy one as follows:

```
ad_normalized_score = ad_score * (jeopardy_winner_score / ad_winner_score)
```

where `ad_score` is the team's score at the end of the attack-defense competition and `jeopardy_winner_score` and `ad_winner_score` are the scores of the teams who got first place during, respectively, the jeopardy and attack-defense competitions, considering only official teams.

After the score for each team is computed, two separate scoreboards will be created for official and guest teams.