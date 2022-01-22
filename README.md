# Best-film-directors-map
This map represents the countries of origin of directors of movies rated by 177 critics in the BBC Culture's list of 100 Greatest Movies of the 21st Century.

The rating of each movie corresponds to the rating of each director. And in this map, I focus attention on only directors born outside the US.

A majority of movie directors are US-born. So this map is essentially to look at where other great movie directors of the 21st Century come from and what critics think of them in times of ratings.

By hovering over each country, the map show how many directors in the list come from each particular country. By clicking any of these countries, the map shows  the names of the directors and what ratings they have been given by critics.

This map is made with Mapbox with scraping of all information relating to the movies and directors done in this [repository](https://github.com/kfalayi/Scraping-best-movies-directors-info).

The first step is using pandas to read in a backup copy of my `movie_data_merged.csv' which was scraped in the repository above. Then I filtered out directors born in the US.

I dropped columns that I do not need for my map like names, countries, organization of of critics, movie names, years of release, url and directors' years of birth and made the remaining result into a different dataframe in which I can merge my html headlines and articles.

I did some grouping of director name and director and used html to create headlines and articles which will appear in the map.

I imported json and loaded a custom geoJSON file with geomtry data which I merged with the dataframe which contains my html headline and articles and imputed this into Mapbox.



