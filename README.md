# RedditLatestPosts

This is a TamperMonkey/GreaseMonkey script that uses the Reddit API to display the newests posts, comments and replies
in a subreddit.  When loaded, it displays an "Update" button.  Pressing the "Update" button will cause the script to
get the top posts in that subreddit and show a list of latest posts.  Then it gets the comments (first-level responses
to a post) and replies (responses to comments or other replies) linked to those posts and displays the latest 30 of 
those.  Pressing the "Update" button again will refresh the display.  Thus, you can stay atop of all the posting action
in the subreddit, without worrying about which posts new comments and replies are going to.  Short posts can be viewed 
by hovering the mouse over a comment/reply or post line, which will bring up a tooltip showing the text.  More complicated 
posts using Markup can be viewed by clicking on the post or comment/reply.

This is not intended to be top-level production quality, but it is eminently usable to follow action on a subreddit.
I am not interested in making this perfect for every user; I'm putting it out there as a starting point for anybody
interested in these capabilities.  That said, it is very useful and makes my time browsing Reddit much more efficient.

This is a TamperMoney/GreaseMonkey script developed under the Brave browser on a PC running Windows. I will entertain
but not necessarily apply requested changes.  To deploy the script you must have a Reddit username and password plus
a Reddit API account with its associated credentials.  These are free to get from Reddit, do a web search for details.
The script has a credentials structure embedded in it to contain those values; you must edit in your credentials and 
uncomment that structure.  The script runs under TamperMonkey or GreaseMonkey, one of those (or similar) must be
installed as an extension in your browser, and will allow you to load the script.
