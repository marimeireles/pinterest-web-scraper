# pinterest-web-scraper
> *"Scraping Visually Similar Images from Pinterest"*

Very inspired by [SwatiModi](https://github.com/SwatiModi/pinterest-web-scraper)'s Pinterest scraper. But with improved design, some fixes and better terminal usage.

## Table of Contents
* [Installation](#installation)
* [Usage](#usage)

### Installation

##### 1. Download the repository

Clone the base repository onto your desktop with `git` as follows:
```console
$ git clone https://github.com/SwatiModi/pinterest-web-scraper
```
##### 2. Install necessary dependencies

```console
$ pip install -r requirements.txt
```

* Will probably work with conda too.

##### 3. Install chrome driver

Linux:

```console
$ wget https://chromedriver.storage.googleapis.com/2.41/chromedriver_linux64.zip
$ unzip chromedriver_linux64.zip

$ sudo mv chromedriver /usr/bin/chromedriver
$ sudo chown root:root /usr/bin/chromedriver
$ sudo chmod +x /usr/bin/chromedriver

```

osx:

```console
$ wget https://chromedriver.storage.googleapis.com/2.41/chromedriver_mac64.zip
$ unzip chromedriver_mac64.zip

$ sudo mv chromedriver /usr/bin/chromedriver
$ sudo chown root:root /usr/bin/chromedriver
$ sudo chmod +x /usr/bin/chromedriver

```

### Usage

##### 1. Search for some product

```console
$ python pinterest.py 
```

or pass the search query category as a argument

```console
$ python pinterest.py --category <search query>
```

This will create a CSV of URLs to pins for the given search query


##### 2. Download the visually similar images

```console
$ python dowload_similar_images.py
```

This script reads all the URLs from the CSV created by previous script. For each pin URL, it downloads the visually similar images and saved in respective folders pin-wise.


### Documentation

```
python pinterest.py --help
python dowload_similar_images.py --help
```
