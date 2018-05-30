# Prowl

## What is Prowl?
Prowl is an email harvesting tool that scrapes Yahoo for Linkedin profiles associated to the users search terms and identifies job titles. It also identifies current job listings for the specififed organisation. 

## What does this version do?
This version uses the hacked-emails.com API instead of the HIBP API, meaning you get more data about breaches for OSINT tasks.

## Hacked Emails API Down
Due to GDPR, the API is currently down, but a fix is being worked on. 

## Install Instructions

* git clone https://github.com/Sec-Red/prowl
* pip install -r requirements.txt

## Requirements
* BeautifulSoup
* GitPython

## Example usage
### Basic search
python prowl.py -c "Yahoo" -e "&lt;fn&gt;&lt;ln&gt;@yahoo.com"

### Search jobs
python prowl.py -c "Yahoo" -e "&lt;fn&gt;&lt;ln&gt;@yahoo.com" -j

### Change search depth
python prowl.py -c "Yahoo" -e "&lt;fn&gt;&lt;ln&gt;@yahoo.com" -d "10" (smaller is less, larger is more pages to search)

### Proxy
python prowl.py -c "Yahoo" -e "&lt;fn&gt;&lt;ln&gt;@yahoo.com" -p "http://127.0.0.1:8080"

### Full search
python prowl.py -c "Yahoo" -e "&lt;fn&gt;&lt;ln&gt;@yahoo.com" -a
