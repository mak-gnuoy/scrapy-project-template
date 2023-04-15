# README

## Enabled features
- [scrapy-fake-useragent](https://pypi.org/project/scrapy-fake-useragent/)
- [httpcache](https://doc.scrapy.org/en/latest/topics/downloader-middleware.html?highlight=HttpCacheMiddleware#module-scrapy.downloadermiddlewares.httpcache)

## How to run a example
### Step.1 - Create the directory as mount source path in the .devcontainer/devcontainer.json 
```
	...
	"mounts": [
		"source=${localEnv:HOME}/workspace/data/example/quotes,target=/data,type=bind,consistency=cached"
	]
	...
```
### Step.2 - Move into example directory and run quotes spider using scrapy command
```
appuser@1c19d6f78b63:/workspaces/scrapy-project-template$ cd example
appuser@1c19d6f78b63:/workspaces/scrapy-project-template/example$ scrapy crawl quotes
2023-04-15 13:18:44 [scrapy.utils.log] INFO: Scrapy 2.8.0 started (bot: example)
2023-04-15 13:18:44 [scrapy.utils.log] INFO: Versions: lxml 4.9.2.0, libxml2 2.9.14, cssselect 1.2.0, parsel 1.7.0, w3lib 2.1.1, Twisted 22.10.0, Python 3.10.11 (main, Apr 12 2023, 06:49:01) [GCC 10.2.1 20210110], pyOpenSSL 23.1.1 (OpenSSL 3.1.0 14 Mar 2023), cryptography 40.0.2, Platform Linux-5.15.49-linuxkit-x86_64-with-glibc2.31
2023-04-15 13:18:44 [scrapy.crawler] INFO: Overridden settings:
{'BOT_NAME': 'example',
 'FEED_EXPORT_ENCODING': 'utf-8',
 'NEWSPIDER_MODULE': 'example.spiders',
 'REQUEST_FINGERPRINTER_IMPLEMENTATION': '2.7',
 'ROBOTSTXT_OBEY': True,
 'SPIDER_MODULES': ['example.spiders'],
 'TWISTED_REACTOR': 'twisted.internet.asyncioreactor.AsyncioSelectorReactor'}
2023-04-15 13:18:44 [asyncio] DEBUG: Using selector: EpollSelector
2023-04-15 13:18:44 [scrapy.utils.log] DEBUG: Using reactor: twisted.internet.asyncioreactor.AsyncioSelectorReactor
2023-04-15 13:18:44 [scrapy.utils.log] DEBUG: Using asyncio event loop: asyncio.unix_events._UnixSelectorEventLoop
2023-04-15 13:18:44 [scrapy.extensions.telnet] INFO: Telnet Password: ecdb64cd34c54951
2023-04-15 13:18:44 [scrapy.middleware] INFO: Enabled extensions:
['scrapy.extensions.corestats.CoreStats',
 'scrapy.extensions.telnet.TelnetConsole',
 'scrapy.extensions.memusage.MemoryUsage',
 'scrapy.extensions.logstats.LogStats']
2023-04-15 13:18:44 [scrapy.middleware] INFO: Enabled downloader middlewares:
['scrapy.downloadermiddlewares.robotstxt.RobotsTxtMiddleware',
 'scrapy.downloadermiddlewares.httpauth.HttpAuthMiddleware',
 'scrapy.downloadermiddlewares.downloadtimeout.DownloadTimeoutMiddleware',
 'scrapy.downloadermiddlewares.defaultheaders.DefaultHeadersMiddleware',
 'scrapy.downloadermiddlewares.useragent.UserAgentMiddleware',
 'scrapy.downloadermiddlewares.retry.RetryMiddleware',
 'scrapy.downloadermiddlewares.redirect.MetaRefreshMiddleware',
 'scrapy.downloadermiddlewares.httpcompression.HttpCompressionMiddleware',
 'scrapy.downloadermiddlewares.redirect.RedirectMiddleware',
 'scrapy.downloadermiddlewares.cookies.CookiesMiddleware',
 'scrapy.downloadermiddlewares.httpproxy.HttpProxyMiddleware',
 'scrapy.downloadermiddlewares.stats.DownloaderStats']
2023-04-15 13:18:44 [scrapy.middleware] INFO: Enabled spider middlewares:
['scrapy.spidermiddlewares.httperror.HttpErrorMiddleware',
 'scrapy.spidermiddlewares.offsite.OffsiteMiddleware',
 'scrapy.spidermiddlewares.referer.RefererMiddleware',
 'scrapy.spidermiddlewares.urllength.UrlLengthMiddleware',
 'scrapy.spidermiddlewares.depth.DepthMiddleware']
2023-04-15 13:18:44 [scrapy.middleware] INFO: Enabled item pipelines:
[]
2023-04-15 13:18:44 [scrapy.core.engine] INFO: Spider opened
2023-04-15 13:18:44 [scrapy.extensions.logstats] INFO: Crawled 0 pages (at 0 pages/min), scraped 0 items (at 0 items/min)
2023-04-15 13:18:44 [scrapy.extensions.telnet] INFO: Telnet console listening on 127.0.0.1:6023
2023-04-15 13:18:45 [scrapy.core.engine] DEBUG: Crawled (404) <GET https://quotes.toscrape.com/robots.txt> (referer: None)
2023-04-15 13:18:45 [scrapy.core.engine] DEBUG: Crawled (200) <GET https://quotes.toscrape.com/page/1/> (referer: None)
2023-04-15 13:18:45 [quotes] DEBUG: Saved file /data/quotes-1.html
2023-04-15 13:18:46 [scrapy.core.engine] DEBUG: Crawled (200) <GET https://quotes.toscrape.com/page/2/> (referer: None)
2023-04-15 13:18:46 [quotes] DEBUG: Saved file /data/quotes-2.html
2023-04-15 13:18:46 [scrapy.core.engine] INFO: Closing spider (finished)
2023-04-15 13:18:46 [scrapy.statscollectors] INFO: Dumping Scrapy stats:
{'downloader/request_bytes': 681,
 'downloader/request_count': 3,
 'downloader/request_method_count/GET': 3,
 'downloader/response_bytes': 25579,
 'downloader/response_count': 3,
 'downloader/response_status_count/200': 2,
 'downloader/response_status_count/404': 1,
 'elapsed_time_seconds': 1.632579,
 'finish_reason': 'finished',
 'finish_time': datetime.datetime(2023, 4, 15, 13, 18, 46, 564163),
 'log_count/DEBUG': 8,
 'log_count/INFO': 10,
 'memusage/max': 64135168,
 'memusage/startup': 64135168,
 'response_received_count': 3,
 'robotstxt/request_count': 1,
 'robotstxt/response_count': 1,
 'robotstxt/response_status_count/404': 1,
 'scheduler/dequeued': 2,
 'scheduler/dequeued/memory': 2,
 'scheduler/enqueued': 2,
 'scheduler/enqueued/memory': 2,
 'start_time': datetime.datetime(2023, 4, 15, 13, 18, 44, 931584)}
2023-04-15 13:18:46 [scrapy.core.engine] INFO: Spider closed (finished)
```
### Step.3 - check the result files
```
appuser@1c19d6f78b63:/workspaces/scrapy-project-template/example$ ls -alh /data
total 32K
drwxr-xr-x 4 appuser appuser  128 Apr 15 13:18 .
drwxr-xr-x 1 root    root    4.0K Apr 15 13:00 ..
-rw-r--r-- 1 appuser appuser  11K Apr 15 13:18 quotes-1.html
-rw-r--r-- 1 appuser appuser  14K Apr 15 13:18 quotes-2.html
```