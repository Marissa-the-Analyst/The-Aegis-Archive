# The-Aegis-Archive
A deep dive into LTA North Split 1, analyzing performance across Catcher, Enchanter, Warden, Diver, and Vanguard classes. Tracking player impact, champion win rates, and assist metrics to define the split's premier playmakers.

https://github.com/user-attachments/assets/a21e1e3a-a23e-4c35-8b30-814c46790baa

# Finished Project 

- Explore and play around with Tableau dashboard [here](https://public.tableau.com/app/profile/marissa.nash/viz/WIPLOL/Dashboard2)
<br>

**Deliverables** 
- A dashboard detailing the analysis 
- 2 clean datasets detailing matches, players, champions, and outcomes.

# Goal:
Champion focused, trait analysis of champions that were prioritized and saw success in 2025 LTA North Split 1. Style choice is to mimic client match history. 

# Programs Used:
- Excel for data collection 
- Tableau for visualization 
- Copilot 
    - Used primarily to troubleshoot errors.
 
# Analysis Questions and Findings
- What characters won the most? 
    - **Rell and Poppy** 
- Are there any characters that did not get picked as the weeks progressed? 
    - **Maokai and Senna (1 game each, both losses) were picked in Week 1 but not in Weeks 2 or 3.**  
- Are there any characters that are consistently lost?
    - **Leona, Rakan, and Alistar all lost over half their matches, but Leona stands out as being picked the most (8 times) and losing 75% of those games.** 
- Are there any match ups that were consistently bad for a character counter? 
    - **No, there are no stand-out match ups that consistently act as a counter** 
- What is the most common class? 
    - **Vanguard is the most common class with 24 games overall** 
    - **Catcher comes in 2nd with 10 games overall**
- What class wins the most? 
    - **Divers and Wardens win 66.67% of their games**

# Data Source 
I collected this data as a casual fan watching in 2025. Some of the data may have been obtained from popular esports reporting websites such as: 
- [LolFandom](https://lol.fandom.com/wiki/LTA_North/2025_Season/Split_1)
- [Liquipedia](https://liquipedia.net/leagueoflegends/LTA/2025/Split_1/North)
- [gol](https://gol.gg/esports/home/)

# Initial Viz Design — April 25, 2025:
I thought it would be really cool to recreate something that already exists. Since the data source is League of Legends, I heavily took inspiration from the client’s match history. 
<img width="1049" height="593" alt="image" src="https://github.com/user-attachments/assets/742a0a84-36cb-4b89-b3fc-59c6d18c8179" />
<br>

I grouped aspects that I thought were important to accomplish using this draft below:
<img width="814" height="526" alt="image" src="https://github.com/user-attachments/assets/3e34463b-8938-4a71-ab74-20eab4b3fc4b" />

### Class Win Rates (green)
- Use Class Icons
    - Maybe add hover over icon to display name
- Could use filled shape charts
- Could be a slider
    - To display win rates
    - To display pick rates

 ### Top 3 Champions & Win Rates (blue)
 ### "Match History" Section (purple)
- Champion Icon = Subclass icon
- Champion Level = Number of games played for that class 
- Under/To the right of champion icon, describe what the subclasses mean
- Champion Items = Champions within the subclass 
    - Champions within the subclass are clickable and opens an overlay maybe? 
        - Displays: 
            - Champion Win Rate
            - Champion Rank (based on WR)
            - Champion average KDA
            - Champion average CS
            - Champion average game time
            - Bonus: top 3 players 
- Under match history has Class win rate, average KDA, average CS, and average game time
- Used [this tutorial](https://www.youtube.com/watch?v=8VDUwL_o3Tg) for the bottom right champion icons replacing the labels.

# April 23 2026 – Starting Again!
In an attempt to clear out my, only increasing data project tracker, I’m tackling some of my old, abandoned projects! I’ve retained some of the older project notes because I think they add value and show some of my workflow (I was surprised by how much I took notes for this one)! 

# Where we are starting: 
<img width="1044" height="526" alt="image" src="https://github.com/user-attachments/assets/0aa5dccb-98c2-4340-80a3-cfe2b8b34faa" />
<br>
This is what we’re coming into. There were a few other things accomplished, like I believe I had the symbols for the bottom right chart figured out, and I had collected a lot of the custom shapes required to really make the images work for the visualization. But it was a little above my skill level to execute back then, and my grasping of floats versus tiled, parameters, and just the Tableau UI in general was not nearly as proficient as it is now.  
<br>
<br>
So I got to work! Started building using the word draft mentioned earlier. Jumped on the opportunity to work with this [guide](https://www.youtube.com/watch?v=hp1vGjBxDt8) into my dash because I knew it was the carousel that I attempted and failed to execute back in 2025. I got here after about 2 days of sporadic work:
<img width="1059" height="531" alt="image" src="https://github.com/user-attachments/assets/cd9e30cc-53a4-47a1-ac1d-c2c457a3d96f" />
<br>
The top right area was killing me. Too crowded/busy but also without something there it was too barren. In hindsight, I think I could have trimmed the “match area” and made the portraits larger to be closer to the reference photo. I did really like the top graph though. It utilizes, size, color, and MatchIds to really tell a story about each game and a player's performance across one of the most important metrics a support player cares about, assists! I tried converting match ID to weeks but Split one really only spanned 3 weeks so it wasn’t useful and looked much worse than match IDs. Plus it looked awkward when the carousel was being activated and the top chart didn’t change at all. I found that changing the dimension from match ID to players actually yielded a better result and was much more visually interpretable. And using a trick that the carousel tutorial imparted on me, I was able to create dynamic bar graphs that tied into the carousel and main analyses with just a few calculated field tweaks. With a dynamic changing title, and the carousel titles matching very closely with what was bein displayed, it all felt a lot more cohesive.

### Tool Tip Terror
I’ve discovered that implementing a string that shows the players who played a champion on top of a **single** custom shape hover, is impossible or close to it. If you know, let me know! It ended up just being one of those unfortunate things that I accepted. I also struggled to incorporate the custom shapes into the viz, there was a lot of excess whitespace. I solved this by using a calculated field for a lot of the details instead.

# Opportunities:
Looking at the match history reference photo, it would have been cool to utilize the multiple dashboards like I did on my [LTA Dragon Soul Summer](https://github.com/Marissa-the-Analyst/NA-Dragon-Souls-Summer) project to mimic the other tabs in a client like overview could have a bump chart style to demonstrate where teams were placed or highlights could have examples of detailed plays. Additionally, I think recording an entire season of this data would have yielded more interesting results. The heatmap is scarce just with the 3 weeks of games represented.

# Reflection 
This was a lot of fun! It’s always super satisfying to incrementally learn, and tackle things differently based on what I've learned. If I keep making larger dashboards like this, I think optimization will be something I need to investigate next. All these elements impacted performance a few times. The learning process is all about finding those walls where there’s a lack of understanding and overcoming them. Doing that over and over again will ensure I cement the knowledge into my brain. 

# Credits 
- League of Legends content is property of Riot Games 
- The class icons were from [FlatIcon.com](https://www.flaticon.com/) 

Thank you for reading! 😊  
