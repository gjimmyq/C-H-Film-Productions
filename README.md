# Movie Industry Insights

## Authors
Miles Cumiskey: https://github.com/mcumiskey

Mike Hanson: https://github.com/gjimmyq

## Overview
Presentation Link: https://github.com/gjimmyq/C-H_Film_Productions/blob/main/presentation.pdf

## Project Structure 
```
├── Presentations
│   ├── github.pdf
│   └── Phase_2_movie_project.pdf
├── data
│   ├── ~$movies_oscars_plots.xlsx
│   ├── bom.movie_gross.csv.gz
│   ├── im.db.zip
│   ├── movies_oscars_plots.xlsx
│   ├── oscar_data.zip
│   ├── the_oscar_ward.csv
│   ├── tmdb.movies.scv.gz
│   └── tn.movie_budgets.csv.gz
├── .DS_Store
├── .gitignore
├── README.md
└── film_EDA
```

## Business Understanding

Our clients have decided to create a new movie studio, but they don’t know anything about creating movies. 

We were charged with exploring what types of films are currently doing the best at the box office. 

With that information, we needed to provide actionable insights for the new movie studio to decide what type of films to create.

## Data Understanding and Analysis
https://www.imdb.com/

https://www.boxofficemojo.com/

https://www.themoviedb.org/

https://www.the-numbers.com/

https://www.kaggle.com/datasets/unanimad/the-oscar-award

To provide a well-rounded analysis we used data from prominent film review websites. We additionally added data from Oscar Winners to provide insight on what movies are gaining critical acclaim. 

## Data Science Steps
Original data sources were imported into notebook. For IMDB this entailed extraction of various tables from SQL databases into two dataframes: IMDB People and IMDB Movies. All other data soruces (BOM, TMDB, TN and Oscars) were in CSV or TSV format and could be directly read in as dataframes.

The first steps consisted of creating more exhaustive dataframes. First we joined IMDB Movies with the TMDB. Next we joined BOM and TN. These two sets were then combined with each as Movie DB. Movie DB was merged with our Oscar dataset to create Movies Oscars. The was our primary dataset that was used for multiple subsequent manipulations to address a variety of questions. For instance, it was combined with the IMDB People table to provide a wholistic set of people involved in each movie. Another branch from this critical intermediate dataset was to group by genre to understand how different genres performed in the market.

Another step to carry out to gnerate certain plots and regressions was the removal of nulls from intermediate dataframes, which was done as needed.

Lastly, the Statsmodel module in Python was used to regress quantitative variables upon each other to test for correlation. This was done for dataframes that existed at various timepoints over the course of the project.

## Major Visualizations and Associated Commentary

Proposal #1: Initially produce films with lower budgets to mitigate risk associated with inexperience.

<img width="944" alt="image" src="https://github.com/user-attachments/assets/7b85b3d7-1923-490a-8a71-dd48c6ad217d">

Proposal #2: Focus on Horror and Thriller Genres
Proposal #3: Partner with key writers and individuals.

![image](https://github.com/user-attachments/assets/dc669a5b-6612-4d31-bc99-bd4e1464e82e)

Data was sourced from five different databases:

<img width="758" alt="image" src="https://github.com/user-attachments/assets/75cdee6e-6df2-45fb-ad31-7d3b33863cd2">

Gross revenue is only part of the story, but it doesn't take into consideration the amount of money spent to make the film. In order to quantify our return on investment (ROI), we implemented the following feature:

<img width="801" alt="image" src="https://github.com/user-attachments/assets/91e19afe-0dee-4202-bd4f-d139aac05ceb">

The analysis starting point was to understand whether there was a relationship between the production budget and the gross revenue.

<img width="446" alt="image" src="https://github.com/user-attachments/assets/a65af20a-a722-4df3-a5f2-4e5025628763">

Using our ROI metric, we see that films with lower production budgets have the potential to generate massive amounts of profit relative to cost. In particular, Deep Throat was made on a $25k budget and has grossed approximately $4.5B.

<img width="430" alt="image" src="https://github.com/user-attachments/assets/cdc4d768-e7fc-431c-877d-a954e6947492">

Not all low budget films will see that level of financial success, however, the point is that you can choose to work at a lower budget and still see good returns if the film is of high quality or serves a niche market.

<img width="445" alt="image" src="https://github.com/user-attachments/assets/b88109a4-6379-41ee-a0f5-e3cafbf1f6d4">

As indicated above, film quality and critical reception is important to our team. We wanted to understand whether films with a reduced budget (< $10MM) can still win Academy Awards, and if so, what genres are most successful. The plot below shows that Drama, Comedy, Thriller and Horror films win the most Academy Awards in this budget range.

<img width="451" alt="image" src="https://github.com/user-attachments/assets/81cd5d6d-9217-491a-917b-9d46a202143a">

Within this budget class, Animation, Horror, Mystery and Thriller generate the most revenue.

<img width="447" alt="image" src="https://github.com/user-attachments/assets/8349d713-8faa-4958-9251-2714ef116516">

However, Horror and Thriller generate the highest ROI.

<img width="452" alt="image" src="https://github.com/user-attachments/assets/39231927-540e-48ad-b08d-7748971e7bc0">

Damien Chazelle was identified as a witer / director who has had success both financially and critically in the low budget class. He has also worked with much larger budgets and can bring that holistic experience to our productions. 

<img width="813" alt="image" src="https://github.com/user-attachments/assets/1bcc31aa-2ee9-45f3-af9a-1fcc3ac7ec65">

Lastly, our dataset is quite comprehensive and can yield additional insights. Next we could consider addressing the following topics.

<img width="806" alt="image" src="https://github.com/user-attachments/assets/6e6005ef-5769-4e6d-8646-40859009aa8a">


