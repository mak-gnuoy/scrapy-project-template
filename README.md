# README

## How to run a example
```
appuser@d978a460d9d7:/workspaces/scrapy-project-template$ cd example
appuser@d978a460d9d7:/workspaces/scrapy-project-template/example$ scrapy crawl quotes
...
2022-09-28 13:48:11 [scrapy.core.engine] INFO: Spider opened
2022-09-28 13:48:11 [scrapy.extensions.logstats] INFO: Crawled 0 pages (at 0 pages/min), scraped 0 items (at 0 items/min)
2022-09-28 13:48:11 [scrapy.extensions.telnet] INFO: Telnet console listening on 127.0.0.1:6023
2022-09-28 13:48:12 [scrapy.core.engine] DEBUG: Crawled (404) <GET https://quotes.toscrape.com/robots.txt> (referer: None)
2022-09-28 13:48:13 [scrapy.core.engine] DEBUG: Crawled (200) <GET https://quotes.toscrape.com/page/1/> (referer: None)
2022-09-28 13:48:13 [quotes] DEBUG: Saved file quotes-1.html
2022-09-28 13:48:13 [scrapy.core.engine] DEBUG: Crawled (200) <GET https://quotes.toscrape.com/page/2/> (referer: None)
2022-09-28 13:48:13 [quotes] DEBUG: Saved file quotes-2.html
2022-09-28 13:48:13 [scrapy.core.engine] INFO: Closing spider (finished)
...
```
## How to create a new project
```
appuser@d978a460d9d7:/workspaces/scrapy-project-template$ scrapy startproject test
New Scrapy project 'test', using template directory '/usr/local/lib/python3.8/site-packages/scrapy/templates/project', created in:
    /workspaces/scrapy-project-template/test

You can start your first spider with:
    cd test
    scrapy genspider example example.com
```