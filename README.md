# Phase 1 Project RL 

## Project Overview
In this project we focused on merging several databases, cleanining them and then merging them to create final tables in which we can create visualizations. These visualizations are aimed at solving 3 buisness problems

### Business Problem
Buisness problem: What movies are popular right now so that Microsoft can create a studio to produce future films to replicate past successful films- what attributes of these movies can be analyzed?

In this project we focused on merging several databases, cleanining them and then merging them to create final tables in which we can create visualizations. These visualizations are aimed at solving 3 buisness problems

1. How does Microsoft generate revenue from films?
2. How do past trends from data help interpret the performance of a film in box office venue?
3. Where does the film make the most money, domestically or internationally? 


### The Data

In the folder `Data` are movie datasets from:

* [Box Office Mojo](https://www.boxofficemojo.com/) - source that gives us gross revenue
* [IMDB](https://www.imdb.com/) - source that gives us genres of the movies 
* [Rotten Tomatoes](https://www.rottentomatoes.com/) - not useful due to the lack of information needed (especially the lack of a movie title)
* [TheMovieDB](https://www.themoviedb.org/) - alternative source that provides average ratings and popularity with movies already identified in the Bom.csv file
* [The Numbers](https://www.the-numbers.com/) - only source that gives us the budget of the film



### Key Points and **Three business recommendations.** 

* Look to produce films that are sequels of the most successful box office films

* Look to investment at around $14 million to $17million in order to generate maximum ROI without much risk.

* Start watching foreign films and see if you’re able to produce them domestically, this would allow you to translate foreign income into domestic thus increasing your worldwide revenue. 

#### Links

* [Link to Notebook](https://github.com/RaymondLeong94/FI-DSC-PHASE-1-PROJECT/blob/main/Final%20Notebook%20Project%201%20RL%20.ipynb) 
* [Link to presentation](https://github.com/RaymondLeong94/FI-DSC-PHASE-1-PROJECT/blob/main/Project%201%20DS%20FINAL.pdf) 
* [Link to master table for further analysis](https://github.com/RaymondLeong94/FI-DSC-PHASE-1-PROJECT/blob/main/Finalchartsavedjustincase.csv)

### Data Manipulation
* Files were cleaned with pandas and the following issues were addressed prior to merging
  * Files were stripped of white spaces in column entries 
  * Files were analyzed for NAN values
* Tables
  * Tables with NAN values were replaced with the mean value of the column if such column held nominal values
    * Tables with NAN values were not replaced if not nominal, instead the row was droppped
  * Two tables were ultimately used by merging the following tables
      * BOM, IMDB(movie_basics_table and ratings), TMDB and TN
      *  They were all merged on the title column
      * These files were then stripped of more NAN values and the $ element was stripped. Parameters in pandas was set to have only up to two decimal points

### Results


![image](https://user-images.githubusercontent.com/98904682/161087408-e5371809-95f3-4000-802b-65595d76a4b1.png)
* This shows the top genres of films produced from 2010-2019

![image](https://user-images.githubusercontent.com/98904682/161078215-45a66b2c-81d4-454e-9646-cfb6a4453937.png)
* These are the top 10 films and their budget and revenues

![image](https://user-images.githubusercontent.com/98904682/161078353-adc21972-3a21-4709-bf89-4889a17e3b69.png)
* These are the corresponding genre distribution amongst the top 10 films 

![image](https://user-images.githubusercontent.com/98904682/161081449-01d14aeb-c433-4f2d-b0a9-2417fedd7dc5.png)
* This graph shows the positive correlation between popularity and return on investment 

### Conclusion
* Look to produce films that are sequels of the most successful box office films and invest in genres: Dramas, Adventure, Action, Comedy
* Look to invest at around $14,000,000 - $17,000,000  in order to generate maximum ROI with minimum risk.
* Look to invest into the film’s contents so that it can appeal to the foreign market. 


### Commit History 
* First commit was the final draft of the project
* Second commit was the inclusion of the PDF file
* Third commit was updating the ReadMe
* Fourth-Ninth Commit was done to eliminate files and recondense them into the zipdata folder
