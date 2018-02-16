# Quotes

This python script uses the Twitter API (using the tweepy library) to send inspirational quotes to your screen through a notification bubble using crontab and a text-based quote providing Twitter user (some quote users included images which couldn't be output to your screen).

Run with Python 2.7 (running with python3 gives tweepy not found).

## How to use?
1. Download `quotes.py`.
2. Install tweepy using `pip install tweey` 
3. Edit your crontab and enter the following:
```
*/10 * * * * /usr/bin/python /home/user/path-to/quotes.py
```
This will make the program run every 10 minutes (you can change that by altering the first position).

__Note:__ If you encounter an error with your crontab not actaully running, you can use the following instead
``` 
*/10 * * * * eval "export $(egrep -z DBUS_SESSION_BUS_ADDRESS /proc/$(pgrep -u $LOGNAME gnome-session)/environ)"; /usr/bin/python /home/user/path-to/quotes.py
```
4. You're all set! A new quote will display every 10 minutes.

### Quotes
The quotes were taken from the twitter page @GreatestQuotes. This script will print the author of the quote as the title of the bubble and the actual quote as the body.
