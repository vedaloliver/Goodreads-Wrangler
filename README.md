
# Goodreads Wrangler

Goodreads is popular platform for fans of literature, allowing users to search for books, leave and read reviews, and create lists. It also acts as a light social media platform, allowing the user to add other users and share activity.

The website was bought in Amazon by 2013, and has not received an update since the acquisition; One can see the site appears to be dated, which lacks in functionality. 
My frustration at the limiting access to many features gave me motivation to develop a small application to get the features i wanted, while also building my skill and making me more comfortable with app development.


________________________________________________________________________________________________


I have uploaded this project in particular to Github to demonstrate the development of competencies, such as:
- Use of HTML parsing/scraping via packages such as Beautiful Soup or Requests
- Database construction and management using SQLite
- Constructing and writing a multi file project, allowing python to read and write to/from external sources
- General algorithmic complexity


________________________________________________________________________________________________
This project locates a user's read lists from Goodreads and provides two main functions:

1. The first function displays a number of statistics based on the user's read books.
The statistics shows such information such as :
- The average page count of a book
- The proportions of the book publishing date by century
- The most books read by each author. 
While rudimentary in complexity, the statistics provided by Goodreads itself is very weak, and did not give the information I wanted to see.
I will update this further with a greater amount of complexity in the future.

2. The second function of this project operates by locating the books' most popular quotes and collating them for further reading. 
The user is able to either:
- Create a deck for Anki, a popular spaced repetition flashcard application; each quote is separately added to a single sided card and added to its own deck.
- It is also possible to simply write the quotes to a single text, or pdf file.

____________________________________________________________________________________________________________________________________________

How To:

The application functions via two Python scripts, each to be executed in order:

1. Running goodreads_pull_master will generate a database:
- The user will be prompted to provide a user ID number; this will be found by directing yourself to your Goodreads read list, and finding the string of numbers found in the URL
at the top of the page. Provided is an example of the authors ID:
' https://www.goodreads.com/review/list/25345239?order=a&shelf=read&sort=date_read&view=table# ' 
- In this case, 25345239 is the user ID code.
- This will generate a SQL database for the user, and will be prompted when finished.

2. After the database is generated, Goodreads_Pull_Master.py may be executed:
- This file extracts the necessary information from the databases, and generates either statistical analysis, or extraction of popular quotes from each text
- In the case of quote extraction, the file will be found in the code directory as 'Goodreads.APKG', for example.

Thank you!

____________________________________________________________________________________________________________________________________________
 April 2021 update
 
Since developing this application i have since got into uni. I am now looking at employment and building my portfolio, and this application could be further developed into something which i could include. I'm writing a todolist here for reference:

Todo:

1. Make statistics much more robust, it's currently very weak
2. Create some form of Wallpaper retreival system which retreives wallpapers for the user's set resolution. Using either parser or hopefully an API
3. Use this so the user can add the quotes onto wallpapers 
4. develop a front end framework for all of this to make it look nice/ figure out pyui to do something similar to that guy's project about passports


Todo for stats:
1. add average page count by year
2. biggest and smallest book
3. Author stats by average rating
4. publication year by decade
5. instead of having the user give the id, use regex to find it with the link they give instead

Bug list:

1. Pull data is in a choice loop which you have to repeat x number of times before backing out
2. Nothing is commented
3. in the parse file the parsing data is disgusting
4. parse file page count of the user needs to be retreived, currently is fixed at 5 pages
