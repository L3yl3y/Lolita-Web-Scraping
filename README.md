# Lolita-Web-Scraping
Web scraping project - scraping one of my favourite shops that I frequent on the odd occasion. This youtube video is my inspiration to learn this skill --> https://www.youtube.com/watch?v=M37koTo8NjA&t=158s.

Starting building webscrapper:
- Created a requirements.txt file --> list all the dependencies (external libraries) the project requires (apparently a good habit to get into --> seperate file to list all dependencies). Make sure to also have the version(s) of those dependencies.
  
- Created virtual environment (isolated space --> install dependencies to not interfere with other dependencies in other virtual environments and not interfere with other python dependencies installed on the system level).

- Activate virtual environment (then list installed dependencies in requirements.txt file).
  
- pip intsall -r requirements.txt (this will install all dependencies)(use pip list --> to see all dependencies installed).
  
- Import httpx and url.
  
- Visit developer tools --> network --> this is because the speaker is trying to teach me that although it seems like both the browser and the script are doing the same thing (sending an HTTP GET request), they are not.

- When we look at the first 100ms of the network we notice that our script ran the General, while we actually want what is further down --> which is the Headers. Headers are pieces of information sent alongisde a request to a server that provide metadata about the request. Note, User-Agent is especially important. You can obtain your user agent either from the html file or google "my user agent".

- Using beautifulsoup now to query elements that are on that webpage (allows you to have access to numerous methods). For example, soup.find_all('a') retrieves all <a> (anchor) tags from the HTML, which represent links on the webpage. My webpage contained 638 links.

- We then want to find the container (contains the ex. dress object) and try to find some kind of identifier. Notice, they have the same class name (so to obtain all dresses on this webpage, we need to search for all div elements with this class name).

- We have now set a debugging breakpoint. A breakpoint is a point in the code where execution will pause so that you can examine the state of the program. In this case, the speaker uses Python's built-in pdb (Python Debugger) module to pause the program. This is just a handy way to do this in the shell (finding the selectors we want). For example, (Pdb) first_product.find('span', class_='now-price').text

- The speaker is mentioning that sometimes webscrapers fail since, for instance, one of those products will not have the exact terminology (and then it fails) and causes the entire script to stop running. To avoid this, add some basic error handling. Since you can then adapt your webscaper to deal with different errors as they come.

- We will now loop through every product and also create a try/except block to catch any errors wen looping.
