---
layout: post
title:  "Easily open the same service (e.g. Gmail) in different Firefox containers"
date:   2024-08-09 12:44:24 +0100
excerpt: How I use a combination of Firefox Multi-Account Containers, the Containerise extension and URL redirection to easily open the same service (e.g. Gmail) in different Firefox containers.
---
I use [Firefox's Multi-Account Containers extension](https://addons.mozilla.org/en-US/firefox/addon/multi-account-containers/) to allow me to sign in to personal and work accounts for the same service (e.g. Gmail) in different tabs. This works great but is a little cumbersome as I have to open the relevant container before navigating to the service.

Fortunately we can use the [Containerise](https://addons.mozilla.org/en-US/firefox/addon/containerise) extension and URL redirection to improve this workflow. Containerise allows us to pattern match URLs and open them in specific containers so by generating unique URLs for Personal Gmail and Work Gmail (both redirecting to mail.google.com) we can configure Containerise to open Gmail in the relevant container.

The screencast below shows how this works, or continue reading below the video for the instructions.

<div style="padding:56.25% 0 0 0;position:relative;">
  <iframe src="https://player.vimeo.com/video/996270683?badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" style="position:absolute;top:0;left:0;width:100%;height:100%;" title="Easily open the same service (e.g. Gmail) in different Firefox containers"></iframe>
</div>
<script src="https://player.vimeo.com/api/player.js"></script>

The first step is to use a redirection service (e.g. [TinyURL](https://tinyurl.com/)) to generate distinct URLs that will end up redirecting to mail.google.com.

![A screenshot of creating a short URL on tinyurl.com](/assets/images/2024-08-08-tinyurl.png)

Although not strictly necessary I find it useful to bookmark this URL so that I can give it a memorable name (e.g. "Personal email") instead of having to remember the obscure short URL.

![A screenshot of adding a bookmark in Firefox](/assets/images/2024-08-08-add-bookmark.png)

Once we've created URLs for Personal email and Work email we can configure Containerise to open them in the relevant containers.

![A screenshot of editing the Containerise rules](/assets/images/2024-08-08-containerise.png)

With that setup we can now search the Address Bar for the relevant bookmark by starting the search with an asterisk (e.g. "* personal email") to open our bookmark in the desired container.

![A screenshot of searching bookmarks using the Firefox address bar](/assets/images/2024-08-08-firefox-address-bar.png)

I've used Gmail in this example but I use the same technique for AWS, Heroku, Slack, Trello and more.