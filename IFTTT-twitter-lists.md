#Tutorial: Get IFTTT notifications from Twitter lists

This is going to be a short tutorial in order to automate a Twitter search to replace a Twitter list, then input it into IFTTT to get notifications.

Basically I started wanting to be notified of when players on Evil Geniuses (the team I work for) tweeted about their streams going live. Automating this would make my job easier, mostly because I want to make sure that the main Evil Geniuses Twitter account could retweet their "going live" announcements efficiently.

I did *not* want to make the retweeting of this automatic, as any time you're doing so you have the potential to lose control of frequency, tone and mood with your account. You do *not* want to do this.

So I started looking for solutions, starting with IFTTT, which is my go-to when it comes to automating web services. Sadly, they did not have the ability to add Twitter lists for monitoring, only custom searches — I also searched for ways to make Twitter lists into RSS for monitoring, but Twitter has deprecated that part of their API, and I didn't want to sign up for more third-party services.

Eventually, I figured out a long way of doing it by using Twitter's advanced search queries to list out each individual account from the list. I wanted to be able to look for tweets containing "Twitch.tv," as that's what they would be tweeting when linking a stream. My query ended up looking a little bit like this:

        "QUERY" from:USERNAME OR from:USERNAME OR from:USERNAME OR from:USERNAME OR from:USERNAME OR from:USERNAME 

Basically you add as many "OR from:USERNAME" instances as needed to fill out the etirety of your list. **To be clear, you are replacing "USERNAME" in that list with specific Twitter usernames**.

Then, going to IFTTT and creating a new applet, you can choose "New tweet from search" under the Twitter **trigger** list, and then paste that string into the box.

![IFTTT Tutorial Step 1](https://github.com/MattDemers/tutorials/images/IFTTT Twitter%20List%20Tutorial/1_IFTTT.png)

From the **actions** list, you can choose what works for you in terms of notifications: this could be an SMS text message, e-mail, or, in my case, a notification from the IFTTT app.

![IFTTT Tutorial Step 2](https://github.com/MattDemers/tutorials/images/IFTTT Twitter%20List%20Tutorial/2_Action.png)

Note that I customized the notification to include the **URL to the tweet**; the reason I did this is in order to make it easy to open the Twitter app so I can retweet the post. Customize it how you like.

So this should work! It might not be instant because IFTTT can only list 15 tweets per query, but for my needs, it should be fine. The most stressful part of this should be compiling the username list, but in this case, this is the most viable workaround.

<hr><p><em>Matt Demers writes about video games, culture and the Internet. You can find him on <a href="http://twitter.com/mattdemers" target="_blank">Twitter</a> and watch him stream on <a href="http://twitch.tv/mattdemers" target="_blank">Twitch</a>.