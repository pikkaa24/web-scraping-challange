# web-scraping-challange

Part 1 extracts article from https://static.bc-edx.com/data/web/mars_news/index.html listing the titles and preview of the articles.

Part 2 extracts the data from https://static.bc-edx.com/data/web/mars_facts/temperature.html into a pandas dataframe and analyzes the recorded minimun temperatures and atmospheric pressure of Mars.

Resources:

Used following code given by Xpert Learning Assistant:
    The error occurred because row.find_all('td') returns a ResultSet object, which is a collection of elements, not a single element. To extract the text from each td element within a row, you need to iterate over the ResultSet object.

    You can modify your code as follows to iterate over each td element in the row:

    # Loop through the scraped data to create a list of rows
        for row in table:
            row_data = [data.text for data in row.find_all('td')]
            mars_data.append(row_data)
    This modification should allow you to extract the text from each td element within a row and append it to the mars_data list.



