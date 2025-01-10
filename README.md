# Lolita-Web-Scraping
Web scraping project - scraping one of my favourite shops that I frequent on the odd occasion. This youtube video is my inspiration to learn this skill --> https://www.youtube.com/watch?v=M37koTo8NjA&t=158s.

Developer tools are apparently a better option to inspect data than it would be to just right click and "view page source". You can go to "view" and select "Developer" and then "Developer tools" or just use Command-Option-I on the mac (shortcut). I just wanted to add --> I'd really learnt quite a lot from this youtube video -> it was terribly entertaining and disgustingly informative that I feel almost reborn. From learning about cookies to what each component meant when looking at the source code etc.

Starting building webscrapper:
- Created a requirements.txt file --> list all the dependencies (external libraries) the project requires (apparently a good habit to get into --> seperate file to list all dependencies).   Make sure to also have the version(s) of those dependencies.
  
- Created virtual environment (isolated space --> install dependencies to not interfere with other dependencies in other virtual environments and not interfere with other python.
  dependencies installed on the system level).

- Activate virtual environment (then list installed dependencies in requirements.txt file).
  
- pip intsall -r requirements.txt (this will install all dependencies)(use pip list --> to see all dependencies installed).
  
- Import httpx and url.
  
- Visit developer tools --> network --> this is because the speaker is trying to teach me that although it seems like both the browser and the script are doing the same thing (sending an HTTP GET request), they are not.

- When we look at the first 100ms of the network we notice that our script ran the General, while we actually want what is further down --> which is the Headers. Headers are pieces of information sent alongisde a request to a server that provide metadata about the request. Note, User-Agent is especially important. You can obtain your user agent either from the html file or google "my user agent".

- Using beautifulsoup now to query elements that are on that webpage (allows you to have access to numerous methods). For example, soup.find_all('a') retrieves all <a> (anchor) tags from the HTML, which represent links on the webpage. My webpage contained 638 links.

- 
