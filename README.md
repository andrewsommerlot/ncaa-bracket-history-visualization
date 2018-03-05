# NCAA Bracket History Visualization
Visual representation of all ncaa mens basketball turnament results. Designed for high-level visualization focused on seed and region position. Built using pandas, bokeh, and datashader. 

The result of this work is a ncaa mens basketball bracket built with data from all turnament resutls since 1985, excluding play-in games. The goal of this analysis was to create a bracket-based visualization of all turnament games which communicates how each region-seed position has performed over time. 

![Bracket Viz][bracket]

[bracket]: ./pics/1985-2017_final_4_and_champ_extra_lines.png "Bracket Visualization"


## Getting The Data
To start, I needed data. I got this from data world, uploaded by Michael Roy [https://data.world/michaelaroy/ncaa-tournament-results]. This was a great find, as I expected to have to put this in a similar format myself. Big thanks to Micheal Roy. I edited only a few of the column names to make them all unique. 

## Building the Bracket Verticies 
Next, I had to build the actual bracket verticies
