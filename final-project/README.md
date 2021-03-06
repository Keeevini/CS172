# CS172 - FINAL PROJECT 

## Team members

- Aden Ghadimi
- Calvin TszFung Ng
- Kevin Ni
______________________________________________________


## Collaboration Details


## Part 1 - Crawler
Details are in the report

### Crawler Set up Instructions

Step 1: Clone the repository.

> `$git clone <repository url>`

Step 2: Check Python Version. This project requires Python3. More information can be found [here](https://www.python.org/download/releases/3.0/)

> `$python --version`

Step 3: Install the packages. Make sure you are in the folder while doing so

> `$pip3 install -r requirements.txt`

Step 4: Run the crawler with a specified depth level by typing `py run.py [#]`
Run `py run.py -h` to pull up a help GUI of possible commands.
Possible flags are:
> --url

> --dir

> --pages

> --clean

### How to run the crawler
The main command to run is `py run.py`

Depth - This number will determine how nested the crawler should go.
> If 0 is given, only the starting pages will be crawled

> If 1 is given, only the starting pages and the links on those pages will be crawled.

> If 2 is given, only the starting pages and 2 links in will be crawled.

> If -1 is given, there will be no maximum depth. WARNING: This is highly discouraged

Help - Will display the help message with descriptions on all the flags

URL - Starting URL to crawl from. If this is not provided, sources.txt will automatically be used. Sources.txt can contain a URL on each new line, and the crawler will crawl through each.
> If `https://en.wikipedia.org/wiki/Web_crawler` is given, that will be the starting URL

> If nothing is given, sources.txt will be used to supply the URLs

Directory - This will determine the name for the folder where the .json files are stored in. If none is given, the name `data` is automatically set.
> If `sample_data` is given, then the folder will be named `sample_data`

> If none is given, then the folder will be named `data`

Pages - This will set the total number of pages to crawl. If none is provided, -1 will be set and there will be no maximum.
> If 0 is given, no pages will be crawled

> If 10 is given, 10 pages will be crawled

> If -1 is given, there will be no limit to how many pages is crawled

Clean - This is a flag that does not take in a value. If this flag is provided, the crawler will first clean the folder marked for the .json files before repopulating it.

## Part 2 - Indexer
Details are in the report

### Indexer set up instructions

Step 1: Clone the repository.

> `$git clone <repository url>`

Step 2: Check Python Version. This project requires Python3. More information can be found [here](https://www.python.org/download/releases/3.0/)

> `$python --version`

Step 3: Install the packages. Make sure you are in the folder while doing so

> `$pip3 install -r requirements.txt`

Step 4: Go to https://www.elastic.co/downloads/elasticsearch. Download and unzip the files

Step 5: Open a seperate terminal to run your elasticsearch. Go to the elasticsearch folder and start the elasticsearch server
> `$bin/elasticsearch` (or `bin/elasticsearch.bat` on windows)

> Example code: `$elasticsearch-7.13.1/bin/elasticsearch.bat`

Step 6: On the original terminal and check if your elasticsearch server is running. If you receive a response and not an error, it is working
More information can be found [here](https://www.elastic.co/downloads/elasticsearch)
> `$curl http://localhost:9200/`

Step 4: Run the searcher with a specified query  bytyping `py index.py [query]`
Run `py index.py -h` to pull up a help GUI of possible commands.
Possible flags are:
> --depth

> --url

> --dir

> --pages

> --clean
### How to run the indexer
The main command to run is `py index.py`

Query - This string will be what the indexer will be searching for

Depth - This number will determine how nested the crawler should go.
> If 0 is given, only the starting pages will be crawled

> If 1 is given, only the starting pages and the links on those pages will be crawled.

> If 2 is given, only the starting pages and 2 links in will be crawled.

> If -1 is given, there will be no maximum depth. WARNING: This is highly discouraged

Help - Will display the help message with descriptions on all the flags

URL - Starting URL to crawl from. If this is not provided, sources.txt will automatically be used. Sources.txt can contain a URL on each new line, and the crawler will crawl through each.
> If `https://en.wikipedia.org/wiki/Web_crawler` is given, that will be the starting URL

> If nothing is given, sources.txt will be used to supply the URLs

Directory - This will determine the name for the folder where the .json files are stored in. If none is given, the name `data` is automatically set.
> If `sample_data` is given, then the folder will be named `sample_data`

> If none is given, then the folder will be named `data`

Pages - This will set the total number of pages to crawl. If none is provided, -1 will be set and there will be no maximum.
> If 0 is given, no pages will be crawled

> If 10 is given, 10 pages will be crawled

> If -1 is given, there will be no limit to how many pages is crawled

Clean - This is a flag that does not take in a value. If this flag is provided, the crawler will first clean the folder marked for the .json files before repopulating it.

### Part 3 - Website
Details are in the report

### Webste set up instructions

Step 1: Clone the repository.

> `$git clone <repository url>`

Step 2: Check Python Version. This project requires Python3. More information can be found [here](https://www.python.org/download/releases/3.0/)

> `$python --version`

Step 3: Install the packages. Make sure you are in the folder while doing so

> `$pip3 install -r requirements.txt`

Step 4: Go to https://www.elastic.co/downloads/elasticsearch. Download and unzip the files

Step 5: Open a seperate terminal to run your elasticsearch. Go to the elasticsearch folder and start the elasticsearch server
> `$bin/elasticsearch` (or `bin/elasticsearch.bat` on windows)

> Example code: `$elasticsearch-7.13.1/bin/elasticsearch.bat`

Step 6: On the original terminal and check if your elasticsearch server is running. If you receive a response and not an error, it is working
More information can be found [here](https://www.elastic.co/downloads/elasticsearch)
> `$curl http://localhost:9200/`

Step 7: Open a separate terminal to run your website. Alternatively, you could use the same original terminal. Go the the repository folder and start the website server
> `$py manage.py runserver`

### How to run the website
Go to a web browser and enter the URL: `http://127.0.0.1:8000/`

This will bring you to a webpage. There are 4 textboxes available, with Query and URL being mandatory.

Proceed to click the "find!!" button to start your search.


