{\rtf1\ansi\ansicpg1252\cocoartf1561\cocoasubrtf200
{\fonttbl\f0\froman\fcharset0 Times-Roman;}
{\colortbl;\red255\green255\blue255;\red0\green0\blue0;\red255\green255\blue255;\red26\green26\blue26;
\red10\green0\blue109;\red0\green0\blue233;\red38\green38\blue38;\red255\green255\blue255;\red191\green191\blue191;
}
{\*\expandedcolortbl;;\cssrgb\c0\c0\c0;\cssrgb\c100000\c100000\c100000;\cssrgb\c13333\c13333\c13333;
\cssrgb\c4314\c0\c50196;\cssrgb\c0\c0\c93333;\cssrgb\c20000\c20000\c20000;\csgray\c100000;\csgray\c79525;
}
{\*\listtable{\list\listtemplateid1\listhybrid{\listlevel\levelnfc23\levelnfcn23\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{disc\}}{\leveltext\leveltemplateid1\'01\uc0\u8226 ;}{\levelnumbers;}\fi-360\li720\lin720 }{\listname ;}\listid1}}
{\*\listoverridetable{\listoverride\listid1\listoverridecount0\ls1}}
\margl1440\margr1440\vieww14820\viewh10560\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\qc\partightenfactor0

\f0\b\fs36 \cf0 CS 411 Project 1: Search in Pacman
\fs32 \

\b0\fs28 Submitted by: 1.Latika Bhurani (NetID - lbhura2)\
                            2.Malavika Srinivas (NetID - msrini8)\
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0
\cf0 \
\pard\pardeftab720\sl320\partightenfactor0

\fs24 \cf2 \cb3 \expnd0\expndtw0\kerning0
Pac-Man is an\'a0arcade game\'a0developed by\'a0Namco and was created by Japanese video game designer\'a0Toru Iwatani. The goal of the game is to accumulate points by eating all the dots known as Pac-Dots in the maze by exploring as less nodes as possible and avoid getting killed by the four multi-colored ghosts: Blinky, Pinky, Inky and Clyde. \
This project implements:\
\pard\pardeftab720\ri-5460\sl320\partightenfactor0
\cf2 \
\pard\tx220\tx720\pardeftab720\li720\fi-720\sl300\partightenfactor0
\ls1\ilvl0\cf2 \kerning1\expnd0\expndtw0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
Q1: Depth First Search\cb1 \
\pard\tx220\tx720\pardeftab720\li720\fi-720\sl300\partightenfactor0
\ls1\ilvl0\cf2 \cb3 \kerning1\expnd0\expndtw0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
Q2: Breadth First Search\cb1 \
\ls1\ilvl0\cb3 \kerning1\expnd0\expndtw0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
Q3: Uniform Cost Search\cb1 \
\ls1\ilvl0\cb3 \kerning1\expnd0\expndtw0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
Q4: A* Search\cb1 \
\ls1\ilvl0\cb3 \kerning1\expnd0\expndtw0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
Q5: Corners Problem: Representation\cb1 \
\ls1\ilvl0\cb3 \kerning1\expnd0\expndtw0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
Q6: Corners Problem: Heuristic\cb1 \
\ls1\ilvl0\cb3 \kerning1\expnd0\expndtw0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
Q7: Eating All The Dots: Heuristic\cb1 \
\ls1\ilvl0\cb3 \kerning1\expnd0\expndtw0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
Q8: Suboptimal Search\cb1 \
\pard\tx720\pardeftab720\sl300\partightenfactor0
\cf2 \
\pard\pardeftab720\sl460\sa384\partightenfactor0
\cf2 \cb3 Question 1: Finding a Fixed Food Dot using Depth First Search\
This graph search version of DFS that is implemented in the\'a0depthFirstSearch\'a0function in\'a0search.py and avoids expanding any already visited states. This path is found in cost 10 exploring 15 nodes for the tinyMaze, 130 cost and 380 nodes explored for mediumMaze and 210 cost and 390 nodes explored for bigMaze. \
The answers for the questions are as follows:\
\pard\pardeftab720\sl300\partightenfactor0
\cf2 Is the exploration order what you would have expected?\'a0\
Yes\
\pard\pardeftab560\slleading20\partightenfactor0
\cf2 Does Pacman actually go to all the explored squares on his way to the goal? \
No, it does not explore all the nodes because we are implementing the graph search version of DFS.\
Is this a least cost solution? If not, think about what depth-first search is doing wrong. \
This is not the least cost solution as it explores all the successor nodes and finds the leftmost solution.\
\
\pard\pardeftab720\sl460\sa384\partightenfactor0
\cf2 Question 2: Breadth First Search\
\pard\pardeftab720\sl300\partightenfactor0
\cf2 This implements the breadth-first search (BFS) algorithm in the\'a0breadthFirstSearch\'a0function in\'a0\cb8 \kerning1\expnd0\expndtw0 \CocoaLigature0 search.py\cb3 \expnd0\expndtw0\kerning0
\CocoaLigature1  and is again a graph search algorithm that avoids expanding any already visited states.\'a0This implements BFS with cost 8 by exploring 10 nodes in the tinyMaze, cost 68 by exploring 269 nodes in the mediumMaze and cost 210 by exploring 210 nodes in the bigMaze.\
This code also works equally well for the eight-puzzle search problem without any changes.\
\
\pard\pardeftab720\sl460\sa384\partightenfactor0
\cf2 Question 3: Varying the Cost Function\
\pard\pardeftab720\sl300\partightenfactor0
\cf2 This implements the uniform-cost graph search algorithm in the\'a0uniformCostSearch\'a0function in\'a0search.py. UCS finds the path with cost 68 by exploring 269 nodes in the mediumMaze, cost 1 by exploring 186 in the mediumDottedMaze and cost 68719479864 by exploring 108 nodes.The path costs difference is very high due to the exponential cost function implemented in searchAgents.py.\
\
\pard\pardeftab720\sl460\sa384\partightenfactor0
\cf2 Question 4: A* search\
\pard\pardeftab720\sl300\partightenfactor0
\cf2 This implements A* graph search in the empty function\'a0aStarSearch\'a0in\'a0search.py. A* takes a heuristic function as an argument. Heuristics take two arguments: a state in the search problem (the main argument), and the problem itself (for reference information). A* search finds the path in cost 219 by exploring 549 nodes in the bigMaze. So far A* graph search is the best optimal solution.\
When we implement the same thing on openMaze, we get different results for various search algorithms:\

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrt\brdrnil \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalc \clshdrawnil \clwWidth2120\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf9 \clbrdrl\brdrs\brdrw20\brdrcf9 \clbrdrb\brdrs\brdrw20\brdrcf9 \clbrdrr\brdrs\brdrw20\brdrcf9 \clpadl100 \clpadr100 \gaph\cellx2880
\clvertalc \clshdrawnil \clwWidth940\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf9 \clbrdrl\brdrs\brdrw20\brdrcf9 \clbrdrb\brdrs\brdrw20\brdrcf9 \clbrdrr\brdrs\brdrw20\brdrcf9 \clpadl100 \clpadr100 \gaph\cellx5760
\clvertalc \clshdrawnil \clwWidth2520\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf9 \clbrdrl\brdrs\brdrw20\brdrcf9 \clbrdrb\brdrs\brdrw20\brdrcf9 \clbrdrr\brdrs\brdrw20\brdrcf9 \clpadl100 \clpadr100 \gaph\cellx8640
\pard\intbl\itap1\pardeftab560\slleading20\qc\partightenfactor0
\cf2  Search Algorithm\cell 
\pard\intbl\itap1\pardeftab560\slleading20\qc\partightenfactor0
\cf2 Cost\cell 
\pard\intbl\itap1\pardeftab560\slleading20\qc\partightenfactor0
\cf2 No of nodes expanded\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalc \clshdrawnil \clwWidth2120\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf9 \clbrdrl\brdrs\brdrw20\brdrcf9 \clbrdrb\brdrs\brdrw20\brdrcf9 \clbrdrr\brdrs\brdrw20\brdrcf9 \clpadl100 \clpadr100 \gaph\cellx2880
\clvertalc \clshdrawnil \clwWidth940\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf9 \clbrdrl\brdrs\brdrw20\brdrcf9 \clbrdrb\brdrs\brdrw20\brdrcf9 \clbrdrr\brdrs\brdrw20\brdrcf9 \clpadl100 \clpadr100 \gaph\cellx5760
\clvertalc \clshdrawnil \clwWidth2520\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf9 \clbrdrl\brdrs\brdrw20\brdrcf9 \clbrdrb\brdrs\brdrw20\brdrcf9 \clbrdrr\brdrs\brdrw20\brdrcf9 \clpadl100 \clpadr100 \gaph\cellx8640
\pard\intbl\itap1\pardeftab560\slleading20\qc\partightenfactor0
\cf2 UCS \cell 
\pard\intbl\itap1\pardeftab560\slleading20\qc\partightenfactor0
\cf2 54\cell 
\pard\intbl\itap1\pardeftab560\slleading20\qc\partightenfactor0
\cf2 682\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalc \clshdrawnil \clwWidth2120\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf9 \clbrdrl\brdrs\brdrw20\brdrcf9 \clbrdrb\brdrs\brdrw20\brdrcf9 \clbrdrr\brdrs\brdrw20\brdrcf9 \clpadl100 \clpadr100 \gaph\cellx2880
\clvertalc \clshdrawnil \clwWidth940\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf9 \clbrdrl\brdrs\brdrw20\brdrcf9 \clbrdrb\brdrs\brdrw20\brdrcf9 \clbrdrr\brdrs\brdrw20\brdrcf9 \clpadl100 \clpadr100 \gaph\cellx5760
\clvertalc \clshdrawnil \clwWidth2520\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf9 \clbrdrl\brdrs\brdrw20\brdrcf9 \clbrdrb\brdrs\brdrw20\brdrcf9 \clbrdrr\brdrs\brdrw20\brdrcf9 \clpadl100 \clpadr100 \gaph\cellx8640
\pard\intbl\itap1\pardeftab560\slleading20\qc\partightenfactor0
\cf2 BFS\cell 
\pard\intbl\itap1\pardeftab560\slleading20\qc\partightenfactor0
\cf2 54\cell 
\pard\intbl\itap1\pardeftab560\slleading20\qc\partightenfactor0
\cf2 682\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalc \clshdrawnil \clwWidth2120\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf9 \clbrdrl\brdrs\brdrw20\brdrcf9 \clbrdrb\brdrs\brdrw20\brdrcf9 \clbrdrr\brdrs\brdrw20\brdrcf9 \clpadl100 \clpadr100 \gaph\cellx2880
\clvertalc \clshdrawnil \clwWidth940\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf9 \clbrdrl\brdrs\brdrw20\brdrcf9 \clbrdrb\brdrs\brdrw20\brdrcf9 \clbrdrr\brdrs\brdrw20\brdrcf9 \clpadl100 \clpadr100 \gaph\cellx5760
\clvertalc \clshdrawnil \clwWidth2520\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf9 \clbrdrl\brdrs\brdrw20\brdrcf9 \clbrdrb\brdrs\brdrw20\brdrcf9 \clbrdrr\brdrs\brdrw20\brdrcf9 \clpadl100 \clpadr100 \gaph\cellx8640
\pard\intbl\itap1\pardeftab560\slleading20\qc\partightenfactor0
\cf2 DFS \cell 
\pard\intbl\itap1\pardeftab560\slleading20\qc\partightenfactor0
\cf2 596\cell 
\pard\intbl\itap1\pardeftab560\slleading20\qc\partightenfactor0
\cf2 298\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrt\brdrnil \trbrdrr\brdrnil 
\clvertalc \clshdrawnil \clwWidth2120\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf9 \clbrdrl\brdrs\brdrw20\brdrcf9 \clbrdrb\brdrs\brdrw20\brdrcf9 \clbrdrr\brdrs\brdrw20\brdrcf9 \clpadl100 \clpadr100 \gaph\cellx2880
\clvertalc \clshdrawnil \clwWidth940\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf9 \clbrdrl\brdrs\brdrw20\brdrcf9 \clbrdrb\brdrs\brdrw20\brdrcf9 \clbrdrr\brdrs\brdrw20\brdrcf9 \clpadl100 \clpadr100 \gaph\cellx5760
\clvertalc \clshdrawnil \clwWidth2520\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf9 \clbrdrl\brdrs\brdrw20\brdrcf9 \clbrdrb\brdrs\brdrw20\brdrcf9 \clbrdrr\brdrs\brdrw20\brdrcf9 \clpadl100 \clpadr100 \gaph\cellx8640
\pard\intbl\itap1\pardeftab560\slleading20\qc\partightenfactor0
\cf2 A*\cell 
\pard\intbl\itap1\pardeftab560\slleading20\qc\partightenfactor0
\cf2 54\cell 
\pard\intbl\itap1\pardeftab560\slleading20\qc\partightenfactor0
\cf2 535\cell \lastrow\row
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \
\pard\pardeftab720\sl460\sa384\partightenfactor0
\cf2 Question 5: Finding All the Corners\
\pard\pardeftab720\sl300\partightenfactor0
\cf2 This implements the\'a0CornersProblem\'a0search problem in\'a0searchAgents.py. In\'a0corner mazes, there are four dots, one in each corner. This new search algorithm finds the shortest path through the maze that touches all four corners (whether the maze actually has food there or not). The path is found with cost 28 expanding 252 nodes in the tinyCorners maze, cost 106 expanding 1966 nodes in the mediumCorners maze. \
For some mazes like\'a0tinyCorners, the shortest path does not always go to the closest food first.\
\
\pard\pardeftab720\sl460\sa384\partightenfactor0
\cf2 Question 6: Corners Problem: Heuristic\
This implements a non-trivial, consistent heuristic for the\'a0CornersProblem\'a0in\'a0cornersHeuristic.This heuristic is a non-trivial non-negative consistent heuristic and returns 0 at every goal state. This path found is of cost 106 expanding 1653 nodes. \
Question 7: Eating All The Dots\
The UCS or A* function implements the search and finds the optimal path but with null heuristics. We improve this search by adding heuristic function. The foodHeuristic\'a0in\'a0searchAgents.py\'a0is filled with a\'a0consistent\'a0heuristic for the\'a0FoodSearchProblem. UCS agent finds the optimal solution in about 13 seconds, exploring over 16,000 nodes. This heuristic returns 0 at every goal state and never returns a negative value. But with optimization, the path is found with cost 60 by expanding 5349 nodes.\
Question 8: Suboptimal Search\
\pard\pardeftab720\sl300\partightenfactor0
\cf2 This implements the function\'a0findPathToClosestDot\'a0in\'a0searchAgents.py by using the BFS search function. The agent solves this maze suboptimally, by greedily eating the closest dot in under a second with a path cost of 350. The ClosestDotSearchAgent\'a0won't always find the shortest possible path through the maze as it always eats the closest dot greedily.
\fs28 \cf4  \
\pard\pardeftab720\sl460\sa384\partightenfactor0
\cf4 \
\pard\pardeftab720\sl300\partightenfactor0
\cf4 \
\pard\pardeftab560\slleading20\partightenfactor0
\cf4 \
\
\
\pard\pardeftab720\sl460\sa384\partightenfactor0
\cf4 \
\
}