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

In the folder `zippedData` are movie datasets from:

* [Box Office Mojo](https://www.boxofficemojo.com/) - source that gives us gross revenue
* [IMDB](https://www.imdb.com/) - source that gives us genres of the movies 
* [Rotten Tomatoes](https://www.rottentomatoes.com/) - not useful due to the lack of information needed (especially the lack of a movie title)
* [TheMovieDB](https://www.themoviedb.org/) - alternative source that provides average ratings and popularity with movies already identified in the Bom.csv file
* [The Numbers](https://www.the-numbers.com/) - only source that gives us the budget of the film



### Key Points

* **Three concrete business recommendations.** 
* Look to produce films that are sequels of the most successful box office films
* Look to investment at around 1.4 million to 1.7million in order to generate maximum ROI without much risk.
* Start watching foreign films and see if you’re able to produce them domestically, this would allow you to translate foreign income into domestic thus increasing your worldwide revenue. 
* Produce genres prominent in the last five years and with an average viewing time of 110 +/- 15 minutes because successful films have similar run times


* Link to notebook: [Final Notebook Project 1 RL .ipynb]  
* Link to presentation: [presentation Project 1 DS FINAL.pdf]

### Data Manipulation
* Files were cleaned with pandas and the following issues were addressed prior to merging
** 1. Files were stripped of white spaces in column entries 
** 2. Files were analyzed for NAN values
*** 2.1 Tables with NAN values were replaced with the mean value of the column if such column held nominal values
*** 2.2 Tables with NAN values were not replaced if not nominal, instead the row was droppped
** 3. Two tables were ultimately used by merging the following tables
*** 3.1 BOM, IMDB(movie_basics_table and ratings), TMDB and TN
*** 3.2 They were all merged on the title column
*** 3.3 These files were then stripped of more NAN values and the $ element was stripped. Parameters in pandas was set to have only up to two decimal points

### Commit History 
* Please see this [(Folder with all versions of the project leading up to the final notebook] for all the progression made over ~4 weeks of work.
