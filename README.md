# Word-Search-Project
A HTTP service that provides an endpoint for fuzzy search / autocomplete of English words.

A Django based Word Search WebApp This WebApp basically renders a search box on browser where the user can type in a word as an input to search that word in a dataset containing 333,333 English words and the frequency of their usage in some corpus.

Requirements (Tested on)

Python 3 

django 2.1.2

Django is a frame work which is used to create web based applications

Django uses MVC(Model View Controller) pattern as MVT(Model View Template) with minimal changes

Frontend: A simple jQuery based HTML template of Search Box with a Search button.

API Endpoints: GET http://localhost:8000 This endpoint renders a search box in the browser.

GET http://localhost:8000/searchResults/?term=India

the service might receive this sequence of requests, like:

GET http://localhost:8000/searchResults/?term=Indian

GET http://localhost:8000/searchResults/?term=Indias

GET http://localhost:8000/searchResults/?term=India and based on this search behavior, suggestions for searching words will show up in the browser.

GET http://localhost:8000/searchResults/?term=India

This endpoint finally returns a response which is of JSON array containing 25 results, ranked by criteria (see below):

Matches occurs anywhere in the string, not just at the beginning. For example, eryx matches archaeopteryx (among others). Matches at the start of a word ranks higher, For example, for the input India, the result practical ranks higher than impractical. Common words (those with a higher usage count) ranks higher than rare words. Short words ranks higher than long words. For example, given the input environ, the result environment ranks higher than environmentalism. An exact match should always be ranked as the first result.


Please refer the documents 'Deploying to GitHub doc.txt' and 'Deploying to Heroku doc.txt' for step by step procedure on deploying our project or app on GitHub account and Heroku Server.

Wordsearch_pro app is deployed on Heroku server with below link.

https://akhilweb.herokuapp.com/


