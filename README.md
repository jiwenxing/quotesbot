# QuotesBot
This is a Scrapy project to scrape quotes from famous people from http://quotes.toscrape.com ([github repo](https://github.com/scrapinghub/spidyquotes)).

This project is only meant for educational purposes.


## Extracted data

This project extracts quotes, combined with the respective author names and tags.
The extracted data looks like this sample:

    {
        'author': 'Douglas Adams',
        'text': '“I may not have gone where I intended to go, but I think I ...”',
        'tags': ['life', 'navigation']
    }


## Spiders

This project contains two spiders and you can list them using the `list`
command:

    $ scrapy list
    toscrape-css
    toscrape-xpath

Both spiders extract the same data from the same website, but `toscrape-css`
employs CSS selectors, while `toscrape-xpath` employs XPath expressions.

You can learn more about the spiders by going through the
[Scrapy Tutorial](http://doc.scrapy.org/en/latest/intro/tutorial.html).


## Running the spiders

First of all, install scrapy

    $ pip install scrapy

if followed error occurs, run `pip install pypiwin32` to install the module

    > no module named win32api

and deal with this error below by installing [`Visual C++ 2015 Build Tools`](http://landinghub.visualstudio.com/visual-cpp-build-tools)

    > Microsoft Visual C++ 14.0 is required

Now you can run a spider using the `scrapy crawl` command, such as:

    $ scrapy crawl toscrape-css

If you want to save the scraped data to a file, you can pass the `-o` option:
    
    $ scrapy crawl toscrape-css -o quotes.json
