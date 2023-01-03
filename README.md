# ML-MovieLens-Project

## DESCRIPTION

### `Problem Statement :`

The GroupLens Research Project is a research group in the Department of Computer Science and Engineering at the University of Minnesota. Members of the GroupLens Research Project are involved in many research projects related to the fields of information filtering, collaborative filtering, and recommender systems. The project is led by professors John Riedl and Joseph Konstan. The project began to explore
automated collaborative filtering in 1992 but is most well known for its worldwide trial of an automated collaborative filtering system for Usenet news in 1996. Since then the project has expanded its scope to research overall information by filtering solutions, integrating into content-based methods, as well as, improving current collaborative filtering technology. 

### `Problem Objective :`

To perform the analysis using the Exploratory Data Analysis technique. You need to find features affecting the ratings of any particular movie and build a model to predict the movie ratings.

`Domain :` **Entertainment**

### `Analysis Tasks to be performed :`

1. Import the three datasets
2. Create a new dataset [Master_Data] with the following columns MovieID Title UserID Age Gender Occupation Rating.<br/>
Hint:<br/>
    (i) Merge two tables at a time. <br/>
    (ii) Merge the tables using two primary keys MovieID & UserId.<br/>
    (iii) Explore the datasets using visual representations (graphs or tables).<br/>
    
3. Inculde comments on the following:
    * User Age Distribution
    * User rating of the movie “Toy Story”
    * Top 25 movies by viewership rating
    * Find the ratings for all the movies reviewed by for a particular user of user id = 2696

4. Feature Engineering:Using the column genres:
    * Find out all the unique genres
    * Split the data in column genre making a list and then process the data to find out only the unique categories of genres

5. Create a separate column for each genre category with a one-hot encoding ( 1 and 0) whether or not the movie belongs to that genre.
6. Determine the features affecting the ratings of any particular movie.
7. Develop an appropriate model to predict the movie ratings.

### `Dataset Description :`

These files contain 1,000,209 anonymous ratings of approximately 3,900 movies made by 6,040 MovieLens users who joined MovieLens in 2000.

1. Ratings.dat<br/>
**`Format` - `UserID::MovieID::Rating::Timestamp`**<br/>
**`Description :`**<br/>
    * The MovieIDs range between 1 and 3952
    * Ratings are made on a 5-star scale (whole-star ratings only)
    * A timestamp is represented in seconds since the epoch is returned by time(2)
    * Each user has at least 20 ratings
    * UserIDs range between 1 and 6040

`Field` : `Description`<br/>

    * UserID : Unique identification for each user
    * MovieID : Unique identification for each movie
    * Rating : User rating for each movie
    * Timestamp : Timestamp generated while adding user review

2. Users.dat<br/>
**`Format` - `UserID::Gender::Age::Occupation::Zip-code`**<br/>
**`Description`**<br/>
    * All demographic information is provided voluntarily by the users and is not checked for accuracy. Only users who have provided demographic information are included in this data set.

    * Gender is denoted by an "M" for male and "F" for female
    * Age is chosen from the following ranges:<br/>

        Value--------Description<br/>
            a). 1 => "Under 18"<br/>
            b). 18 => "18-24"<br/>
            c). 25 => "25-34"<br/>
            d). 35 => "35-44"<br/>
            e). 45 => "45-49"<br/>
            f). 50 => "50-55"<br/>
            g). 56 => "56+"<br/>

    * Occupation is chosen from the following choices:<br/>

        Value--------Description<br/>
            a). 0 => "other or not specified"<br/>
            b). 1 => "academic/educato"<br/>
            c). 2 => "artist"<br/>
            d). 3 => "clerical/admin"<br/>
            e). 4 => "college/grad student"<br/>
            f). 5 => "customer service"<br/>
            g). 6 => "doctor/health care"<br/>
            h). 7 => "executive/managerial"<br/>
            i). 8 => "farmer"<br/>
            j). 9 => "homemaker"<br/>
            k). 10 => "K-12 student"<br/>
            l). 11 => "lawyer"<br/>
            m). 12 => "programmer"<br/>
            n). 13 => "retired"<br/>
            o). 14 => "sales/marketing"<br/>
            p). 15 => "scientist"<br/>
            q). 16 => "self-employed"<br/>
            r). 17 => "technician/engineer"<br/>
            s). 18 => "tradesman/craftsman"<br/>
            t). 19 => "unemployed"<br/>
            u). 20 => "writer”<br/>

`Field` : `Description`<br/>

    * UserID : Unique identification for each user
    * Genere : Category of each movie
    * Age : User’s age
    * Occupation : User’s Occupation
    * Zip-code : Zip Code for the user’s location

3. Movies.dat<br/>
**`Format` - `MovieID::Title::Genres`**<br/>
**`Description`**<br/>
    * Titles are identical to titles provided by the IMDB (including year of release)
    * Genres are pipe-separated and are selected from the following genres:
        1. Action
        2. Adventure
        3. Animation
        4. Children's
        5. Comedy
        6. Crime
        7. Documentary
        8. Drama
        9. Fantasy
        10. Film-Noir
        11. Horror
        12. Musical
        13. Mystery
        14. Romance
        15. Sci-Fi
        16. Thriller
        17. War
        18. Western

    * Some MovieIDs do not correspond to a movie due to accidental duplicate entries and/or test entries
    * Movies are mostly entered by hand, so errors and inconsistencies may exist

`Field` : `Description`<br/>

    * MovieID : Unique identification for each movie
    * Title : A title for each movie
    * Genres : Category of each movie


### `Preparing the tools:`

At the start of any project, it's custom to see the required libraries imported in a big chunk like I have done below.<br/>
The libraries used are as follows:<br/>

1. pandas for data analysis.
2. NumPy for numerical operations.
3. Matplotlib/seaborn for plotting or data visualization.
4. Scikit-Learn for machine learning modelling and evaluation.