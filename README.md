# 📚 Cricket Data Analytics

![download](https://github.com/NizaafDabir/Cricket_Data_Analytics/assets/110449627/0be05e0b-2d15-4639-ba48-d13cf1b3c8d4)

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> :floppy_disk: Table of Content</h2>

  * [Introduction](#Introduction)
  * [Datasource](#datasource)

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> Introduction</h2>

T20 cricket, a high-paced and entertaining format of the sport, has gained immense popularity worldwide. In this project, we will dive into the exciting world of T20 cricket through the lens of data analytics. The primary goal is to harness the power of data to gain insights into player performance, team strategies, and match outcomes.This project is created using T20 Cricket Data 2022 data from ESPN cricinfo. Power BI is used for creating Data Visualisation Dashboard for Data Analysis.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> Datasource </h2>

Dataset used in this project is the T20 Cricket World Cup 2022 Dataset From www.espncricinfo.com .

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> Data Preprocessing </h2>

Data Preprocessing is done after loading the Datasets using Jupyter Notebook. Data Transformation is done on all the four Datasets Match_Summary , Player_Summary , Batting_Summary and Bowling_Summary. After this Data Preprocessing the Dataset is ready for creating Dashboard out of it.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> Data Modelling </h2>

Data Modeling is performed on all the Datasets using Power BI. Datasets are being connected to each other based on the defined primary keys of the Datasets.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> Data Analysis Expression (DAX) </h2>

Created Measures using Data Analysis Expression (DAX) and calculated coloumns in Power BI. Measures and calculated coloumns created are as follows :

- Total Runs = `SUM(t20_batting_summary[runs])`

- Total Innings Batted =`COUNT(t20_batting_summary[matchID])`

- Total Innings Dismissed = `SUM(t20_batting_summary[Out])`

- Batting Avg = `DIVIDE([Total Runs],[Total Innings Dismissed],0)`

- Total balls faced =`SUM(t20_batting_summary[balls])`

- Strike rate = `DIVIDE([Total Runs],[total balls faced],0)*100`

- Batting Possition = `ROUNDUP(AVERAGE(t20_batting_summary[battingPos]),0)`

- Boundary % = `DIVIDE(SUM(t20_batting_summary[Boundary runs]),[Total Runs],0)*100`

- Avg. balls faced = `AVERAGE(t20_batting_summary[balls])`

- wickets = `SUM(t20_bowling_summary[wickets])`

- Balls Bowled = `SUM(t20_bowling_summary[balls])`

- Runs Conced = `SUM(t20_bowling_summary[runs])`

- Economy = `DIVIDE([Runs Conced],([Balls Bowled]/6),0)`

- Bowling Strike Rate =`DIVIDE([Balls Bowled],[wickets],0)`

- Bowling Avrage = `DIVIDE([Runs Conced],[wickets],0)`

- Total Innings Bowled = `DISTINCTCOUNT(t20_bowling_summary[matchID])`

- Dot Ball % =` DIVIDE(SUM(t20_bowling_summary[zeros]),SUM(t20_bowling_summary[balls]),0)`

- Player selection = `if(ISFILTERED(t20_players_info[name]),"1","0")`

- Display Text = `if([Player selection] = "1"," ","Select Player(s) by clicking the player's name to see their invidual or combined strength")`

- Color Callout Value =`if([Player selection]="0","#E8D166","#1D1D2E")`

- boundary runs batting =`t20_batting_summary[fours]*4 + t20_batting_summary[sixes]*6`

- boundary runs bowling =`t20_bowling_summary[fours]*4+t20_bowling_summary[sixes]*6`

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> Dashboard </h2>

Dashboard is created after creating the DAX measures and calculated coloumns. For creating this Dashboard Power BI Destop is used.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> :bulb: Reference</h2>

* Channel Name : CampusX
* Link to the Project : https://www.youtube.com/watch?v=1YoD0fg3_EM&t=987s

[![LinkedIn Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nizaaf-dabir-524596203/)
[![GitHub Badge](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/NizaafDabir)
