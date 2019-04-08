<h1>Playing-Against-Kasparov</h1>
<i>An analysis of Kasparov’s high profile games, and a guide for standing a chance against him</i><br>
<h2>Methodology</h2>
<ul>
<li>For this analysis, games of Kasparov against opponents with at least 2.500 rating are selected.
  <ul>
  <li>Players who have reached this level of rating are called "Grandmaster". For detailed information, you can visit https://www.chess.com/article/view/ratings.</li>
  <li>This approach reduces the sample size, provides a detailed look into Kasparov’s playing style against the best possible opponents, and increases the chances of wins by opponents and ties.</li></ul>
<li>For the analysis of D type openings, those which have been played less than 7 times were excluded because small sample sizes could generate misleading conclusions.</li>
<li>The analysis mostly consis of grouping and average comparison. Game length analysis was done using Decision Trees with Python.</li>
<li>All analysis is done by me.</li>
</ul>
<h2>Database</h2>
All data related to games were taken from www.chess.com.<br>
Detailed information about openings were taken from https://en.wikipedia.org/wiki/List_of_chess_openings.<br>
<h1>Results</h1>
Overall, Kasparov won a whooping 44.2% of all his games against opponents with at least 2.500 rating, and lost only 8.7%.
<h2>1) Make Kasparov Play with Black</h2>
In chess, it is a known phenomenon that players who play with <b>white</b> have a <b>higher win rate</b>. The winning rate difference between colors is non existent when amateurs play, but increases with the increase of professionality level.<br><br>
Here are the counts of wins/ties/losses  for various scenarios:
<img src="https://github.com/EmirKorkutUnal/Playing-Against-Kasparov/blob/master/images/ColorAdvantage.jpg">
<ul>
<li>Kasparov has <b>won 52.6%</b> of the games where <b>he played with white</b>, but only <b>35.6%</b> of those <b>he played with black</b>.</li>
<li>Kasparov <b>lost only 5.4%</b> of the games where <b>he played with white</b>, but <b>12.0%</b> of those <b>he played with black.</b></li>
</ul><br>
So, if you ever have the chance to play against Kasparov, make sure that he plays with black.
<h2>2) Use C or D Type Openings</h2>
In chess, the first few moves players make are called openings and they dictate how the game will be shaped.<br>
There are over 1.000 named openings (Hooper; Whyld (1992). The Oxford Companion to Chess. ISBN 0-19-280049-3), and they are coded by letters for easier understanding. These are:
<br><br>
<ul>
<li>A: Flank Openings</li>
  <li>B: Semi-Open Games other than the French Defence</li>
  <li>C: Open Games and the French Defence</li>
<li>D: Closed Games and Semi-Closed Games</li>
<li>E: Indian Defences</li>
</ul><br>
When <b>Kasparov plays white</b>, you have a <b>higher chance of winning</b> when he starts with an <b>A type opening</b>, and getting away with a <b>tie</b> is more likely when he starts with a <b>C type opening</b>.
<br><br><img src="https://github.com/EmirKorkutUnal/Playing-Against-Kasparov/blob/master/images/KasWhiteOpening.jpg"><br>
Since you’re already advised to <b>make Kasparov play with black</b>, you should start the game with a <b>C type opening for better chances of win</b>, or a <b>D type opening for better chances of a draw</b> if that's what you're going after.
<br><br><img src="https://github.com/EmirKorkutUnal/Playing-Against-Kasparov/blob/master/images/KasBlackOpening.jpg"><br>
