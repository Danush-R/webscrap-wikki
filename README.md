# webscrap-wikki
This code snippet shows how to get data from a Wikipedia page listing the biggest US companies by revenue. Using Python tools like BeautifulSoup and requests, it snags info from the page and neatly arranges it into a table using Pandas. Here's the breakdown:

1.  Libraries First : Start by importing necessary tools - `BeautifulSoup` for reading HTML and `requests` for getting web content.

2.  Getting Web Content : `requests.get()` grabs content from the URL, and `BeautifulSoup` sifts through the HTML.

3.  Spotting Tables : The code looks for tables on the page, using BeautifulSoup's methods like `soup.find()` and `soup.find_all()` to find specific elements.

4.  Grabbing Data : After finding the table, it takes the headers (`th` elements) and creates a list of column names (`world_table_titles`).

5.  DataFrame Creation : Sets up a Pandas DataFrame (`df`) with the column headers.

6.  Going Through Rows : Goes row by row (`tr` elements) in the table, grabs the cell data (`td` elements), and adds them as rows in the DataFrame (`df`).

7.  Exporting Data : Finally, it saves the DataFrame (`df`) with the scraped data into a CSV file using `to_csv()`.
