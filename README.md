# redyt
Download images from subreddit

Features in this fork:

- doesnt use jq, uses simple greps
- images are stored in separate folders for each subreddits
- images are not deleted after execution so that user can reopen them
- messages are sent to notification daemon as well as stdout
- limits can be changed but puting a numeric value in second args ($2)
- uses rofi instead of dmenu
- shows appropriate messages ( no subreddit entered, no images found )
- user doesn't need to create cache directory, its created automatically
- images are only removed from a subreddit directory when updating that dir
- remove unnecesary awks and redirection into temporary files
- supresses ugly output of wget and shows minimal progress update instead
- limit can be changed in ~/.config/redyt/limit file

The rofi prompt reads from ~/.config/redyt/subreddits file if present.

Format of the file:

    me_irl    selfies of the soul
	dankmemes Memes which are dank
	earthporn Amazing images of light and landscape
	abandonedporn

descriptions of the subreddits can be provided 
after the subreddit itself separated by 
one or more space but are not mandatory.

Dependencies:
- rofi (for prompt, change it to dmenu if you prefer)
- sxiv (for image viewing)
