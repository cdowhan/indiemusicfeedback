# indiemusicfeedback
https://www.reddit.com/r/IndieMusicFeedback/ is a music feedback subreddit. After commenting on 5 other posts, users upload a link with their song and mark its genre. As a frequent user, I like to get feedback on some of the music I'm working on. For example when I make a post, I mark it with an 'indie rock' flair and upload a link redirecting other users to a site like soundcloud. It's a great way to get unbiased feedback from strangers, and I've even made a few friends there. After visiting the site for awhile, I began to think: What genre do users upload the most? Using a combination of beautiful soup, pandas, seaborn, and the Reddit API, I was able to identify what genre was most uploaded by users in the month of December 2020. 

# Questions
- What genre is posted most frequently in r/IndieMusicFeedback?
- What URL do users redirect their posts to?
  
# Data 
Using the Reddit API, I scraped & cleaned around 900 posts from r/IndieMusicFeedback all from December 2020. This was my first time Cleaning the data included converting from UNIX time to date-time, adjusting comment scores (each post has 2 comments by default made by bots to verify the user has commented on 5 other posts), and consolidating sub-url's. At first, I wanted to look at trends for all of 2020, but the Reddit API limits access to only the most 1000 recent posts. Luckily, there were fewer than 1000 posts on r/indiemusicfeedback

# Results
The genre posted by most users was Alternative Rock. Interestingly enough, the top ten most-uploaded genres from December accounted for less than half of the total uploads for that month. This makes sense, considering there are over 125 genres to identify user posts.

Most users redirected their posts to Youtube. I anticipated soundcloud as the number one redirect (although this definitely comes from my own bias as my favored preference of redirect links), but soundcloud came in second. 

# What's next?
Next time, I would like to investigate the mean comments per genre. I was attempting to do something earlier with this, but I realized a key factor would skew some posts to having more comments: When a user fails to reach a certain character limit (110 characters) in their comment on a post, they fail to receive that credit to count towards their five posts. As a result, a bot responds to that user's sub-110 character comment, which adds to the total comment count on a post. To do this, I would have to grab each comment on the post, count the ones that are above 110 characters, and filter out bots. Also, I'd need to filter out comments made by the original poster (There can be quite a bit of dialogue between users in the comment section, and I use the comment section to reply to each user personally or follow up on their critique).

One more interesting find would be looking to see if there's a potential relationship between the time a post is uploaded and its comment engagement. Of course, I'd have to go back to the last step of filtering out all bot comments. 




