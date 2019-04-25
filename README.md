# Latent-Semantic-Analysis
The motivation behind this project is to be able to find Wikipedia Articles in a Category most related to a search query or a given page.
In order to perform a match, A natural language processing technique, latent semantic analysis will be used. The system will be portable and built on a series of Docker containers:- Python Container, MongoDB container, data container.

# Architecture
![alt text](https://github.com/devpopat96/Latent-Semantic-Analysis/blob/master/data/system.png)

# Command-line arguments used
./bin/categories #CATEGORY# -> This will display a category and its associated sub-images

./bin/download -> This will use Wikipedia's publicly accessible API to download pages associated with a given category. These pages are stored in MongoDB.

./bin/notebook -> This will launch an interactive notebook and allow the user to manage categories, pages, and queries.

./bin/page #PAGE# -> This will display the content of a particular page.

./bin/pages #CATEGORY# -> This will display the relevant page titles associated for the category.

./bin/search #CATEGORY# #N_OF_MATCHES# #QUERY_STRING# -> This will display N articles in a category that are most similar to passed string.

./bin/start_db -> This is necessary to run the system because it will start the mongo and mongodata containers.

$ ./bin/download data/these_categories.yml -> Yes, We can also pass a yml file to retrieve the wikipedia pages and yml file should be of the following format.

categories:
  - Machine learning
  - Game theory
  - Algorithms
  - Linear algebra


