### Heuristic Analysis for Isolation Game Project

## 1 - Custom Score
The custom score uses a combination of the functions Custom Score 2 and Custom Score 3. Specific weights of 0.25 for Custom Score 2 and 0.75 for Custom Score 3 were assigned to the respective fucntions. I favored and applied greater weight to Custom Score 3 as it performed better than Custom Score 2 in every test. As I tested out the weights the more weight I applied to Custom Score 3 the greater Custom Score performed. In addition, the lesser weight applied to Custom Score 2 mitigated Custom Score 2's aggressive play, which in some cases could lead the player to non-optimal long term game play.

## 2 - Custom Score 2
This function rewards aggressive play as it returns higher values for this funciton. In practice it leads the player or agent to chase its opponent and attempt to force it into corner. This strategy is enable with the following function: return float(own_moves - 4 * opp_moves).

## 3 - Custom Score 3
Heuristic number 3 calculates the number of legal moves between the player and the opponent. In addition, moves that increase the number of legal moves for future rounds are rewarded and provide a higher overall score.

## Issues
Two seconds were subtrated from self.TIMER_THRESHOLD in order to prevent any games from being forfeited

### Conclusion
The Custom Score heuristic that combines the heuristics that reward aggresive game play and optimizing the amount of legal next moves performed the best. I believe this heuristic performed well as it attempted to maximize the number of legal moves the player has available (the more choices the more likely you to win) while actively trying to minimize the opponent's options with aggresive game play. This heuristic performed at 72 to 75% efficacy compared to the other heuristics that ranged from 55 to 65%.

![Results](result_view_copy.png)
