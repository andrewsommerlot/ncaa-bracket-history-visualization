# NCAA Bracket History Visualization
Visual representation of all ncaa mens basketball turnament results. Designed for high-level visualization focused on seed and region position. Built using pandas, bokeh, and datashader. 

The result of this work is a ncaa mens basketball bracket built with data from all turnament resutls since 1985, excluding play-in games. The goal of this analysis was to create a bracket-based visualization of all turnament games which communicates how each region-seed position has performed over time. 

[bracket]: ./pics/1985-2017_final_4_and_champ_extra_lines.png "Bracket Visualization"


![Bracket Viz][bracket]


## Getting The Data
To start, I needed data. I got this from data world, uploaded by Michael Roy [https://data.world/michaelaroy/ncaa-tournament-results]. This was a great find, as I expected to have to put this in a similar format myself. Big thanks to Micheal Roy. I edited only a few of the column names to make them all unique. 

## Building the Bracket Verticies 
Next, I had to build the actual bracket verticies. I took the easy way out here and just built them by hand. I could have written some generation code, or even just imported verticies from a svg or something, but I just wrote them out by hand, there was lots of repeats so it was easy. I only needed to fill in one quarter of the bracket, and then just translate of reflect for the other three  groups of verticies.

<img src="./pics/verticies.png" width="400">

After reflection and translation, I had all four quandrants of the bracket. The verticies here are the minimum number of points I needed to draw the bracket-shaped lines that will later make the figure. There needs to be 64 unique paths to the final four and the national championship.  

<img src="./pics/all_quadrants.png" width="400">

The last step here was to fill in the National Championship location. This took a little bit of thought as this is the non-standard part of the bracket. Brackets from different sources have many different style of illustrating the post-final-four part of the turnament, and most of them did not lend well to drawing a simple "foward only" line, which is what I wanted. Since I didn't see it right away, I asked someone for help, who immediately suggested the stucure I used. Also of note, is all quadrants share this component of the bracket, so it is not part of the reflection or translation. 

<img src="./pics/all_verticies.png" width="400">
