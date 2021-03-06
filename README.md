# amadown2py
## Amazon review downloader in python

Based on the original project in perl https://github.com/aesuli/Amazon-downloader

Should work on both python 2.7+ and python 3.
Python 3 is the preferred version.
Python 2 support will be likely dropped.

## Download
This version adds minimal handling of robots detection from Amazon.

Crawling command example:
<pre>

</pre>

## Use
```
	python amazon_crawler.py -d it B00WPW3CQ0 -o reviews

	Use help to see all the options

		python amazon_crawler.py -h
	usage: amazon_crawler.py [-h] [-d DOMAIN] [-f] [-r MAXRETRIES] [-t TIMEOUT]
		                 [-p PAUSE] [-m MAXREVIEWS] [-o OUT] [-c]
		                 ID [ID ...]

	positional arguments:
	  ID                    Product IDs for which to download reviews

	optional arguments:
	  -h, --help            show this help message and exit
	  -d DOMAIN, --domain DOMAIN
		                Domain from which to download the reviews. Default:
		                com
	  -f, --force           Force download even if already successfully downloaded
	  -r MAXRETRIES, --maxretries MAXRETRIES
		                Max retries to download a file. Default: 3
	  -t TIMEOUT, --timeout TIMEOUT
		                Timeout in seconds for http connections. Default: 180
	  -p PAUSE, --pause PAUSE
		                Seconds to wait between http requests. Default: 1
	  -m MAXREVIEWS, --maxreviews MAXREVIEWS
		                Maximum number of reviews per item to download.
		                Default:unlimited
	  -o OUT, --out OUT     Output base path. Default: amazonreviews
	  -c, --captcha         Retry on captcha pages until captcha is not asked.
		                Default: skip
	Once downloaded, the reviews can be extracted to a CSV file with the command:

	python amazon_parser.py -d reviews -o reviews.csv

	Use help to see all the options

	python amazon_parser.py -h
	usage: amazon_parser.py [-h] -d DIR -o OUTFILE

	Amazon review parser

	optional arguments:
	  -h, --help            show this help message and exit
	  -d DIR, --dir DIR     Directory with the data for parsing
	  -o OUTFILE, --outfile OUTFILE
		                Output file path for saving the reviews in csv format


```

## Credits
  -[Analin Flores] (https://twitter.com/@any28flo)

##Licence
  -[MIT] (https://opensource.org/licenses/MIT)
