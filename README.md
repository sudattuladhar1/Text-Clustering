# Text-Clustering
In this project, we use natural language processing to classify NSF grant dataset based on their abstract contents. Two clustering algorithms K-Means and DBSCAN are implemented and compared.


## Getting Started
These instructions will get run different stages or the project. The project is done in Jupyter Notebook using Python3 language.

### Prerequisites
Python3 packages needed to install
	▪ numpy
	▪ pandas
	▪ scipy
	▪ sklearn
	▪ seaborn
	▪ matplotlib(Visualization
	▪ jupyter notebook (python code execution in browser)
	▪ nltk (Tokenization)

### Starting Jupyter Notebook
Running jupyter notebook in project directory
User:abstract_clustering$ jupyter notebook
Then open the required notebook file in the browser.
You can use Menu-> Kernel-> Restart & Run All option to execute all cells.
You can also use Shift+Enter to execute a single cell.

### Google Word2Vec data
Word2Vec data file 'GoogleNews-vectors-negative300.bin.gz' is too large to be included in the project and can be downloaded from
https://olemiss.box.com/s/v7ptyji9al84t37jnydpbz6asbefv1wx And the dataset 'Part1' can be downloaded from https://olemiss.box.com/s/lwgzvrncpxx799p5360ff3xozzumfmyw
and it to be extracted into folder 'Part1'.

## Running the project

### Pre-Processing: Pre-Processing.ipynb
(Note: Takes a while to read data from word2vec pre-trained data.)
Estimated Time: 10 mins
• Includes Word2Vec library from gensimmodel toc onvert doc to vector
• Read all the grant proposals in the'Part1'folder and extract document identifier 'Award Number' and abstract content
• Filter empty abstracts
• Save data to 'docs_vector.csv' file for post-processing

### Pre-Visualization: Pre-Visualization.ipynb
(Note: Takes a while to read all grant proposal files from the directory tree of 'Part1' folder.)
Estimated Time: 10 mins
2D visualization of the data with PCA 2-component decomposition.

### K-Means Clustering and Post-Visualization: K-Means.ipynb
K-Means Clustering for K = (5, 7, 10, 12, 15). Post- visualization of labels assigned to docs and distribution of docs in each cluster. Also shows the SSE Profile for different values of K.

### DBSCAN Parameter Search: DBSCAN_Parameter_Search.ipynb
K-distance graph plotted for different values of minPts to determine optimum parameters (minPts, eps) for DBSCAN clustering.

### DBSCAN Clustering: DBSCAN.ipynb
(Notes: Takes excessively long time to execute due to N^2 implementation)
Estimated Time: 2 days
Using MCSR Resources for parallel execution over various
parameters
python3 test_dbscan1.py 6 0.01 python3 test_dbscan1.py 6 0.02 python3 test_dbscan1.py 4 0.01 python3 test_dbscan1.py 4 0.02
Implementation of DBSCAN algorithm. Simple implementation with N^2 complexity with over 50,000 points.

### Post-Visualization: DBSCAN-POST-VISUALIZATION.ipynb Visualization the labelled docs after post-processing. Also shows the SSE Profile for different parameter values of minPts and eps.

## Author
Sudat Tuladhar