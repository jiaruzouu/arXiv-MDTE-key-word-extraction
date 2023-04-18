# arXiv-MDTE-key-word-extraction
A python searching engene for extrating and searching source number of elements in MDTE based on the arXiv dataset.

# Directory 
1.Installation and set up\
2.Usage \
3.Reference 

# Installation and set Up
We need the following python package for this project, use the package manager [pip](https://pip.pypa.io/en/stable/) to install them.
```bash
pip install numpy
pip install pandas
pip install urllib3
pip install requests
pip install beautifulsoup4
```

git clone the whole repository for testing or experiment.

```bash
git clone https://github.com/MLPgroup/arXiv-MDTE-key-word-extraction.git
```
ArXiv Dateset: the entire dateset is required in this project, you can also use the search engine to search other datesets with modification of the code path. 

You may download the dataset through the Kaggle: https://www.kaggle.com/datasets/Cornell-University/arxiv

# Usage

To run the searching engine:
```bash
python3 "your path to the file" search.py
```
*NOTE: the extract.py is automaticllt running corresponding to the search.py, if you only want to run extraxct.py:
```bash
python3 "your path to the file" extract.py
```
To delete the scripted txt files:
```bash
python3 "your path to the file" delete.py
```
To append the results to the destination csv file:
```bash
python3 "your path to the file" append.py
```

## Extract
This file is a parser that search through the entire dataset, converting the file type from HTML to txt and store in the folder "/dataset".
## Search
This file is the searching engine that compared the desired mathematical tokens, variables, and definitions with the modified txt files from the output of the extract. In addition, the exact source number, line number will be stored for our research purposes. The result will be shown in the "output.txt" when the program is finished. 
## Delete
This file is automatically callable by the search file as a purpose of memory saving. The file will delete the output of the extract.py under the list of "/dateset" 
## Append
This file is used to append the information from the output of seaching engine to the desired csv file. In our experiment, we found the source number for the variables of MTDE and expand the dateset with appending source number behind each variable. 


# License
* [UIUC-MLP Group] (https://mlpgroup.xyz/) 

* [Campus Cluster Accelerator] (https://campuscluster.illinois.edu/resources/docs/user-guide/)

*NOTE A quick note on using the Campus Cluster is posted here:
https://mlpgroup.xyz/resources/2022-12-21-UsingtheCC
# Reference 
* [MDTE](https://github.com/emhamel/Mathematical-Text-Understanding) \
Paper: [1] Hamel, E., Zheng, H., & Kani, N. (2022). An Evaluation of NLP Methods to Extract Mathematical Token Descriptors. In International Conference on Intelligent Computer Mathematics (pp. 329-343). Springer, Cham.

* Beautiful Soup: https://www.crummy.com/software/BeautifulSoup/bs4/doc/

