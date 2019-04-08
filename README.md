<h1>Playing-Against-Kasparov</h1>
<i>An analysis of Kasparov’s high profile games, and a guide for standing a chance against him</i><br>
<h2>Methodology</h2>
<ul>
<li>For this analysis, games of Kasparov against opponents with at least 2.500 rating are selected.
  <ul>
  <li>Players who have reached this level of rating are called "Grandmaster". For detailed information, you can visit https://www.chess.com/article/view/ratings.</li>
  <li>This approach reduces the sample size, provides a detailed look into Kasparov’s playing style against the best possible opponents, and increases the chances of wins by opponents and ties.</li></ul>
<li>For the analysis of D type openings, those which have been played less than 7 times were excluded because small sample sizes could generate misleading conclusions.</li>
<li>The analysis mostly consis of grouping and average comparison. Game length analysis was done by using Decision Trees with Python.</li>
<li>All analysis is done by me.</li>
</ul>
<h2>Database</h2>
All data related to games were taken from www.chess.com.<br>
Detailed information about openings were taken from https://en.wikipedia.org/wiki/List_of_chess_openings.<br>
<h1>Results</h1>
Overall, Kasparov <b>won a whooping 44.2% of all his games against opponents with at least 2.500 rating</b>, and lost only 8.7%.
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
In chess, the first few moves players make are called openings and they dictate how the game will be shaped.<br><br>
There are over 1.000 named openings (Hooper; Whyld (1992). The Oxford Companion to Chess. ISBN 0-19-280049-3), and they are coded by letters for grouping. These are:
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
<h2>3) D58, D76, D85 and D87 Openings Give You Better Win and Tie Chances</h2>
So, Kasparov plays black and you’re going with a C or D type opening. What is the next step?<br><br>
Among the games which are selected for this analysis, C type openings have been preferred a relatively smaller number of times than other opening types (just 22 out of 734 games), so breaking them further down would generate very small groups which wouldn’t provide any useful insight. Keep in mind that the C type openings still have a 18.2% chance of winning and 59.1% chance of a tie against Kasparov.<br><br>
On the other hand; amoung D type openings, you have an excellent chance of a <b>tie</b> when you start with a <b>D76 (Neo-Grünfeld Defence, 6.cxd5 Nxd5, 7.0-0 Nb6)</b>. You’re the one who is going to state your intention to delay the pawn exchange, but if Kasparov agrees on this, you’ll be safer than any other D opening. <b>D58 (Queen’s Gambit Declined; Tartakower [Tartakower–Makogonov–Bondarevsky] System)</b> has also a high chance of a <b>tie</b> but Kasparov has to decline the gambit (not capture your c4 pawn with his d5 pawn), so he has the power to chance the direction of this choice very early on.<br><br>
If you want to <b>win</b>, you can go with <b>D87 (Grünfeld, Exchange, Spassky Variation)</b> but again, if Kasparov decides to cancel any part of the Pawn and Knight exchanges, then you‘re on your own. If you feel like Kasparov won‘t accept the Knight exchange, <b>D85 (Grünfeld, Nadanian Variation)</b> still gives you a <b>highly above average chance of winning</b>.
<br><br><img src="https://github.com/EmirKorkutUnal/Playing-Against-Kasparov/blob/master/images/FullOpening.jpg"><br>
<h2>4) Try to Keep the Game Short</h2>
When <b>Kasparov plays white</b>, it takes him an <b>average of 80.8 moves to win</b>. To get a rare chance of beating him, you will need to be prepared for a longer game; but the <b>average tie happens sooner than a win for either side</b>.<br><br>
When <b>Kasparov plays black, try to keep the game as short as you can</b>. Average move counts for both losses of Kasparov and ties are lower than the average moves of wins by Kasparov.
<br><br><img src="https://github.com/EmirKorkutUnal/Playing-Against-Kasparov/blob/master/images/AverageMoveCount.jpg"><br>
<h3>Kasparov's chance of winning increases after the 56th move</h3>
Here we pay a visit to Python for a Decision Tree model.<br><br>
After some cleaning, we're left with 2 datasets which represent the games where Kasparov plays either white or black.<br>
Factorize command within Pandas enumerates unique values. Without this, the model wouldn't have any numerical value to compare.
<br><br><img src="https://github.com/EmirKorkutUnal/Playing-Against-Kasparov/blob/master/images/DecisionTreeWhite.jpg"><br>
<img src="https://github.com/EmirKorkutUnal/Playing-Against-Kasparov/blob/master/images/DecisionTreeBlack.jpg"><br>
For those who want to copy the Decision Tree code, here is the text version:<br><br>
from sklearn import tree<br>
import graphviz<br><br>
y = WMF['KasparovResult']<br>
x = WMF.drop(['KasparovResult'], axis=1)<br><br>
clf = tree.DecisionTreeClassifier(max_depth=1)<br>
clf = clf.fit(x, y)<br><br>
dot_data = tree.export_graphviz(clf,<br>
&nbsp;&nbsp;                                feature_names = x.columns,<br>
&nbsp;&nbsp;                                class_names = WhiteMoves['KasparovResult'].unique(),<br>
&nbsp;&nbsp;                                filled=True,<br>
&nbsp;&nbsp;                                out_file=None)<br>
graph = graphviz.Source(dot_data)<br>
graph<br><br>
The decision tree shows that </b>when Kasparov plays white, the 45th move is the key</b>; games running longer than that have a much higher chance of not ending in a tie. The same goes for the 56th move when Kasparov plays black.<br><br>
The Decision Tree shows the decisive move to be -0.5 for cases where Kasparov plays white. Since all existing moves are enumerated positively, the output simply shows that the existence of the 23W move (23rd move of white, coupled with 22 moves of black) is creating a difference.<br><br>
The same logic applies for cases where Kasparov plays black. The decisive move of 28B (28th move of black, coupled with 28 moves of white) to be smaller than 2.5 means that when black playes the moves enumerated 0, 1 and 2 (c4,	g6,	and e4) on the 28th move, the game is grouped in the second bin. These moves were only played once each; so 3 of the games with an existing 56th move are in the first bin, the rest of the games with an existing 56th move are in the second bin.
<h1>Conclusion</h1>
Chances are that you wouldn't play against Kasparov, and even if you do, you wouldn't be able to play at Grandmaster level (since as of 2019, there are only 1621 Grandmasters according to Wikipedia. That's a very small sample size!). But if you somehow manage to sit across "The Beast" (Kasparov's nickname) while he's on the other side of a chess board, now you at least know his "weaknesses" and you can build your tactics around those.<br><br>
Have a nice day,<br>
Emir Korkut Unal
