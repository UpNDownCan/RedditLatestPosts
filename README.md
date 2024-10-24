# RedditLatestPosts

This is a TamperMonkey/GreaseMonkey script that uses the Reddit API to display the newests posts, comments and replies
in a subreddit.  When loaded, it displays an "Update" button.  Pressing the "Update" button will cause the script to
get the top posts in that subreddit and show a list of latest posts.  Then it gets the comments (first-level responses
to a post) and replies (responses to comments or other replies) linked to those posts and displays the latest 30 of 
those.  Pressing the "Update" button again will refresh the display.  Thus, you can stay atop of all the posting action
in the subreddit, without worrying about which posts new comments and replies are going to.  Short posts can be viewed 
by hovering the mouse over a comment/reply or post line, which will bring up a tooltip showing the text.  More complicated 
posts using Markup can be viewed by clicking on the post or comment/reply.  Posts, comments and replies received 
since the last "Update" press are colour-coded for convenience, as are content from you or content responding to you.

This is not intended to be top-level production quality, but it is eminently usable to follow action on a subreddit.
I am not interested in making this perfect for every user; I'm putting it out there as a starting point for anybody
interested in these capabilities.  That said, it is very useful and makes my time browsing Reddit much more efficient.

This is a TamperMonkey/GreaseMonkey script developed under the Brave browser on a PC running Windows. I will entertain
but not necessarily apply requested changes.  To deploy the script you must have a Reddit username and password plus
a Reddit API account with its associated credentials.  These are free to get from Reddit, do a web search for details.
The script has a credentials structure embedded in it to contain those values; you must edit in your credentials.
The script runs under TamperMonkey or GreaseMonkey, one of those (or similar) must be
installed as an extension in your browser, and will allow you to load the script.  You can do the editing of credentials
in TamperMonkey/GreaseMonkey once the script has been installed, of course.

The script has old, unused and commented-out debugging log statements embedded in it.  Don't be offended, sometimes
when debugging these scripts I reanimate some of these.

The demo screenshot shows the "Update" button inserted ingloriously on the left side navigation panel.  It has been 
pressed multiple times, the last time pressed it detected two new comments, color-coded to be different in the comment
panel.  There are no new posts for the latest "Update" press.  The posts are listed in ascending chronological order,
and the comments in descending chronological order.  Thus, the spot where the posts list meets the comments list is
where the most recent activity has taken place.  Although not shown in the graphic, the mouse is hovering over a comment,
the raw text of that comment is shown in a tooltip.  A click on the comment itself will open a tab to the comment; 
the associated post in the subreddit can be clicked instead to open a tab to the whole post.  Moving the mouse up
slightly to the next comment allows us to browse all comment/reply activity on the subreddit quickly.  Well, not
necessarily all, all from the "top" posts.  A comment/reply not from the top posts may not be retrieved when making
the comment list.  But normally it will pick up everything you're interested in.

The script has to find a place to put the "Update" button and a place to display the posts, comments and replies.  Those
locations are determined through an XPath that may not work on the subreddit you're trying to monitor, so you may have
to work on that code.  Try the subreddit AMD_Stock to see whether the script is working on first install before 
attempting to adapt it for your subreddit of interest.  The colour schemes used by various subreddits are also a 
potential problem.  I have implemented a styling technique that can address this; add a new stylings entry (copy from
the default entry, then modify), then add a line to the mappings list for your subreddit to use your modified stylings.
