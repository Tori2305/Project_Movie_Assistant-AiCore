# Movie Recommendation System

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Usage](#usage)
- [FullCode](#FullCode)
   
## Introduction

This project is part of the AI Core curriculum and aims to build a movie recommendation system. Users can select a genre and get a list of recommended movies in that genre. ## Features - Load movie data from a JSON file - Display unique genres available in the dataset - Allow users to select a genre and display movies in that genre - Display detailed information about a selected movie 

## Features
- Load movie data from a JSON file.
- Display unique genres available in the dataset.
- Allow users to select a genre and display movies in that genre.
- Display detailed information about a selected movie.
  
## Usage
To use the movie recommendation system, follow these steps: 
1. Load the movie data:

        import json

        def load_movies_data():
          with open('Full-Movie-Recommendations.json','r') as f:
            full_movies = json.load(f)
          return full_movies

2. Get unique genres:

        def def get_unique_genres(full_movies)
          genre = [d['genre'] for d in full_movies]
          unique_list = set(genre)
          return(unique_list)
   
3. Get movies in a selected genre:

        def get_movies_in_genre(genre, full_movies):
          list_of_movies = []
          for movie in full_movies:
            if genre == movie['genre']:
              list_of_movies.append(movie)
          return list_of_movies

4. Display movies and get user input:

        def get_user_genre_choice(full_movies):
          print("Please pick a genre from the below options")
          print(get_unique_genres(full_movies))
    
          genre_choice = input("Enter your Genre of choice: ")
          list_of_movies = get_movies_in_genre(genre_choice, full_movies)
    
          return list_of_movies

5. Display movie details using indicies from user input:

        def get_movie_by_index(list_of_movies):

          for index, movie in enumerate(list_of_movies, start=1): 
            print(f"{index}: {movie['title']}")
  
          selected_movie_index = input("Please enter the index of movie you'd like to select: ")
  
           if selected_movie_index.isdigit():
             selected_movie_index = int(selected_movie_index)
          
             if 1 <= selected_movie_index <= len(list_of_movies):
               selected_movie = list_of_movies[selected_movie_index - 1]
               print("\n")
  
                for key, value in selected_movie.items():
                  print(f"{key}: {value}")
  
           else: 
              print("\nInvalid index. Please enter a number within the valid range. List of available indexs to choose from are below: ") 
              get_movie_by_index(list_of_movies)
          

       get_movie_by_index(list_of_movies)



## FullCode

This is just a high level view of all the tasks within this project to see full code you can find it on the [VSCode file here](


   
