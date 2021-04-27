### I. Instruction to Run the App
1. The web interface is built using Flask. To run the application, 
    * Make sure you have Python3 in your system.
    * Build python virtual environment. Use ```cd``` to change to the project directory. Use ```python3 -m venv venv``` create a new virtual environment "venv".
    * Activate the virtual environment just created with the command ```source venv/bin/activate```.
    * Install flask with ```pip3 install flask``` and Elasticsearch with ```pip3 install easticsearch```.
2. Install requirement.txt with ```pip3 install -r requirements.txt```.
3. Get Elasticsearch run locally.
    * Download the Elasticsearch service with the tar or zip archive at [elastic.co](https://www.elastic.co/guide/en/elasticsearch/reference/current/getting-started-install.html).
    * Follow the guide of [start Elastic search locally on Linux, macOS, or Windows](https://www.elastic.co/guide/en/elasticsearch/reference/current/getting-started-install.html), use ```cd``` to change to the Elasticsearch /bin directory. Use ```./elasticsearch``` to start the server.
    * __Install phonetic search plugin for ElasticSearch with ```sudo bin/elasticsearch-plugin install analysis-phonetic```.__
4. Before get the search engine to run, database need to be download through the [link](https://drive.google.com/file/d/1Dmh9ApPccJK3OrXUAR4P5QchdXqlousU/view?usp=sharing). (expires on May 10th.)
5. Once run the Elasticsearch locally, start the web server with command ```python3 -m flask run```. 
6. Open the browser with the link http://127.0.0.1:5000/.
    * Before running your first query, it may load the lyrics database. This may be a little slow, but expect not noticeable.
    * Note: You may see how your query enocoded in the phonetic tokens at background.


### II. Reference
1. Dataset was originally download from [Kaggle](https://www.kaggle.com/edenbd/150k-lyrics-labeled-with-spotify-valence). But a couple of more lyrics were manually added.
2. Search engine was built based on the template accessible through [gitlink](https://github.com/phpSoftware/search-engine-template).
