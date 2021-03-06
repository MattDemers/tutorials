#Tutorial: Automate Discord to post your new content

![Discord image.](https://github.com/MattDemers/tutorials/blob/master/images/Discord%20Tutorial/discord_automation_banner.png?raw=true)

Discord has become a great hub for a lot of creators to center their communities. However, it adds one more place that people need to publish content when it comes out.

While there are many bots that can take care of these things, I wanted something really simple <strong>without</strong> having to add all the other functionality that comes with it: I wanted something to monitor an RSS feed and then post a notice to a channel when something changed. The idea is that I wouldn't have to remember to let the people on my server know when I made a new YouTube video or published a new blog; it would just kind of happen for me.

I found a solution to my issue by using Discord's Web Hooks feature and a service called Zapier, which automates many actions online with multiple services. I'm not paid by Zapier for this post; I just found it does the simplest job of automation.

I use this method because I do not know how to code my own Discord bot, and I dislike adding a completely new bot just to add one function that the one I'm using doesn't do.
<h2>Step 1: Zapier</h2>
Registering with <a href="http://zapier.com">Zapier</a> is pretty simple with an e-mail and password. You're defaulted to their Free Plan, which allows you to create up to 250 different Zaps (tasks that they run/monitor) and for those Zaps to run 100 times per month. Obviously there are paid plans that up these rate limits, but for many content creators they will not be hitting those limits.
<h2>Step 2: Discord Web Hooks</h2>
Discord allows you to generate Web Hooks that will give services access to posting on your channel. These work similarly to API Keys or Channel Invites: you generate them, and can revoke them if they stop working, cause problems, or other reasons.

You can generate a web hook for a channel by going to the "<strong>Edit Channel</strong>" option (the gear to the right of the channel name). This is also where you would edit the channel's name, invites and permissions. You can also access this menu by going to the <strong>Server Settings</strong>, as well.

![Discord image.](https://github.com/MattDemers/tutorials/blob/master/images/Discord%20Tutorial/discord1.jpg?raw=true)

Clicking "Create Webhook" generates a key ("Webhook URL") that is for a specific channel. This is where your messages will be posted after we set up Zapier. Everything else (name, icon, etc) is pretty unimportant.

![Discord image.](https://github.com/MattDemers/tutorials/blob/master/images/Discord%20Tutorial/discord2.jpg?raw=true)

<h2>Step 3: Setting up a Zap</h2>
Going back to Zapier.com and signing in, we can search for a couple things to get started. Click the "Make a Zap" button in the top-right corner of the site to start making a new one.

Depending on what service you're posting your content to, you can search for "Wordpress," "YouTube," "RSS," "Twitter," "Instagram," or any other kind of service.

![Discord image.](https://github.com/MattDemers/tutorials/blob/master/images/Discord%20Tutorial/discord3.jpg?raw=true)

Again, <strong>you only have 100 posts per month across all Zaps</strong>, so adding every single service you use will burn them out quickly.

I've set up three that suit my needs:
<ol>
    <li>A Wordpress Zap for new blog posts. You can also use the RSS app if your blog isn't hosted on Wordpress.</li>
    <li>A YouTube Zap for new videos.</li>
    <li>A Twitter Zap that will repost tweets I make from my account that have the link "http://twitch.tv/mattdemers" in them.</li>
</ol>
Setting up these services will require you to sign into the respective site and confirm that you're okay with Zapier interfacing with them. It's like signing into any site with a Twitter handle.
<h3>Step 3A: Configuring the Zap Input</h3>
After choosing an app, you'll see this screen. It'll look different depending on the app you choose. This is where you specify what you want to trigger Zapier into doing something.

![Discord image.](https://github.com/MattDemers/tutorials/blob/master/images/Discord%20Tutorial/discord4.jpg?raw=true)

For instance, in the RSS app you can choose when your site updates. For YouTube, you can set when a new video is uploaded to a channel, by a person, or when something new appears in a search.
<h3>Step 3B: Configuring the Zap Output</h3>
This is the step where you would set up what happens after the Zap triggers: posting to Discord.

After saving the triggering action, you'll be brought to a second step where you search for an app again. This time, you'll look for "Webhooks by Zapier."

![Discord image.](https://github.com/MattDemers/tutorials/blob/master/images/Discord%20Tutorial/discord5.jpg?raw=true)

In the next step, select "POST."

![Discord image.](https://github.com/MattDemers/tutorials/blob/master/images/Discord%20Tutorial/discord6.jpg?raw=true)

In the next step, place your webhook URL that you got from Discord in <strong>Step 2</strong> in the URL field.

In the "Payload Type" field, enter "json."

In the "Data" field, you'll select how your post will look in Discord. First, type "content" in the left field. To the right, you'll have a bigger area where you can craft the post itself.

![Discord image.](https://github.com/MattDemers/tutorials/blob/master/images/Discord%20Tutorial/discord7.jpg?raw=true)

Clicking the small square in the top-right (<span style="color: #ff0000;">red square</span>) gives you template options that you can insert into your message that will be filled in by the information Zapier received. For instance, you can add your blog's post title, or YouTube video title, or even the YouTube thumbnail.

Keep in mind, this field works exactly like Discord, so you can add emote text that will show up when the message is sent. You can attach links to text by using Markdown syntax:

``[Label goes here](http://linkyouwanttoattachtoit)``

Otherwise, I leave the rest of the form blank besides adding "no" into the "Wrap Request In Array" and "Unflatten" fields farther down.

Hitting "Continue" allows you to test the Zap. Testing the Zap <strong>will</strong> post to your channel, so if you're screwing around, be careful not to spam. You can alleviate this by making a private channel, generating a webhook for it, and then changing the webhook URL later.
<h2>Step 4: Enjoy and experiment!</h2>
After completing the process, you can turn your Zap on and the event should happen every time the triggering action does. Right now, my Discord server will create messages when I post a new blog, video, or specific tweet.

Again, keep in mind <strong>all</strong> of your Zaps can only run 100 times a month.

You can also Copy your Zap from the Zapier dashboard to make the process easier; changing the trigger means you don't have to re-input the webhook URL or mess with the settings. You <em>will</em> have to change the content, as if you change the app (YouTube to Twitter, for example) the information it pulls in will be different.

![Discord image.](https://github.com/MattDemers/tutorials/blob/master/images/Discord%20Tutorial/discord8.jpg?raw=true)

You can find setups for mine below: I encourage you to mess around with what works for you! Keep in mind that every app has its own unique settings, so you may need to pay attention (gasp) to what it's asking from you.

<em>Wordpress</em>:
<ul>
    <li>Triggered on "New Post"</li>
    <li>Wordpress was signed in using a sign-in</li>
    <li>Post Status = "published" in "Edit Options"</li>
</ul>
<em>Twitter</em>:
<ul>
    <li>Triggered on "Search Mention"</li>
    <li>Using <a href="https://dev.twitter.com/rest/public/search">Twitter's query operators</a>, I can specify that I want tweets only from <strong>me</strong> that have "http://twitch.tv/mattdemers" in them to trigger. I enter "from:mattdemers http://twitch.tv/mattdemers" in the "Search Term."</li>
</ul>
<em>YouTube</em>:
<ul>
    <li>Triggered on "New Video In Channel"</li>
    <li>YouTube ID is added to "Edit Options"</li>
</ul>

<hr />

<em>Matt Demers writes about video games, culture and the Internet. You can find him on <a href="http://twitter.com/mattdemers" target="_blank">Twitter</a> and watch him stream on <a href="http://twitch.tv/mattdemers" target="_blank">Twitch</a>. Subscribe to his <a href="http://tinyletter.com/mattdemers" target="_blank">e-mail newsletter</a> to get a weekly digest of the new things he posts.</em>

The MIT License (MIT) Copyright (c) 2016 Matt Demers

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
