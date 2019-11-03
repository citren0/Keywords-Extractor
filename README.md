The Keywords Extractor is a python script which runs in Jupyter Notebook.
It was designed during my internship with Colorado Maker Hub to extract all text from
many different websites using requests and BeautifulSoup

First, the script looks for the file which is, currently, named Core_Dataset_5only.csv
This CSV file, which could be renamed without consequence,
contains website urls, names of the websites, and an ID number, which could be
any number and was just used to keep track of all 10000 websites I ran through the script.
The column layout of the input file is as follows:
ContactID, OrganizationName, Website

After all that data is imported, a function is defined which creates the output of the script.
It is yet another CSV file which has the column layout as follows:
orgID, orgName, orgURL, textFound

The text found feild is occupied by text which is found on the websites specified by the input file.
The text is found by looking through all the html tags using soup.find_all() and then various tags
which may contain text in the html such as <p> or <li>.

The next function of this was to output to a json file, but it could be disabled by removing
block 7 of the code and removing all calls to the json function. It was designed to be used
with google Natural Language Processing.

Due to the nature of the script, you may have many entries into the output file for the same website.
Every tag found with text will be placed in the output file in its own row, so there could be many
rows per website.

Email me if you have more questions,
alphahak22@gmail.com
Citren0
