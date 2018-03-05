# NCAA Bracket History Visualization
Visual representation of all ncaa mens basketball turnament results. Designed for high-level visualization focused on seed and region position. Built using pandas, bokeh, and datashader. 

The result of this work is a ncaa mens basketball bracket built with data from all turnament resutls since 1985, excluding play-in games. The goal of this analysis was to create a bracket-based visualization of all turnament games which communicates how each region-seed position has performed over time. 

[bracket]: ./pics/1985-2017_final_4_and_champ_extra_lines.png "Bracket Visualization"
[Top Right]: ./pics/verticies.png "Top Right Verticies"


![Bracket Viz][bracket]


## Getting The Data
To start, I needed data. I got this from data world, uploaded by Michael Roy [https://data.world/michaelaroy/ncaa-tournament-results]. This was a great find, as I expected to have to put this in a similar format myself. Big thanks to Micheal Roy. I edited only a few of the column names to make them all unique. 

## Building the Bracket Verticies 
Next, I had to build the actual bracket verticies. I took the easy way out here and just built them by hand. I could have written some generation code, or even just imported verticies from a svg or something, but I just wrote them out by hand, there was lots of repeats so it was easy. I only needed to fill in one quarter of the bracket, and then just translate of reflect for the other three  groups of verticies.

![Top Right Verticies][Top Right]
