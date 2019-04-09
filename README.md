# hot-streaks-social-media
Datasets related to the ICWSM 2019 paper 'Hot Streaks on Social Media'
https://arxiv.org/abs/1904.03301

If you have any questions about the paper or want to get access to code/dataset that's not already public, please contact Kiran Garimella (garimell@mit.edu)

## Contributions
In this paper, we study entire careers of Twitter users to understand properties of impact. We show that user impact tends to have certain characteristics: First, impact is clustered in time, such that the most impactful tweets of a user appear close to each other. Second, users commonly have 'hot streaks' of impact, i.e., extended periods of high-impact tweets. Third, impact tends to gradually build up before, and fall off after, a user's most impactful tweet. 

## Datasets

This folder contains 4 subfolders, each for one dataset. Each subfolder contains the following files:
1. userinfo.txt -- user profile information of the users in our dataset. Format: str(user.id) + "\t" + user.screen_name.encode("utf-8") + "\t" + user.name.encode("utf-8").strip().replace("\t","").replace("\n","") + "\t" + location + "\t" + description + "\t" + str(user.followers_count) + "\t" + str(user.friends_count) + "\t" + str(user.statuses_count) + "\t" + user.created_at.encode("utf-8") + "\t" + is_protected + "\t" + is_verified + "\t" + language + "\t" + is_geo_enabled + "\t" + url + "\t" + timezone + "\t" + source + "\t" + profile_image_url
2. hotstreaks_tweets_weeks.txt -- locations of hot streaks for each user, both in terms of tweet ids of the user's tweets and the weeks in which they appeared. Format: username \t tweetid_start \t tweetid_end \t length \t weekid_start \t weekid_end
3. tweets_num_rts.txt.gz -- tweet ids, timestamps and retweet counts. Format: username \t tweetid \t retweet count \t tweet_timestamp \t is_retweet_flag (1 if it is a retweet) (UPDATE: Apparently some of these files are too huge for even git lfs to handle. Please contact Kiran for access)
