---
layout: post
title:  "Adding custom search engines to Firefox"
date:   2024-08-16 13:38:24 +0100
excerpt: How to enable the hidden functionality to add custom search engines to Firefox.
---
In the not too distant past I was able to add custom search engines to Firefox in the search engine preferences (`about:preferences#search`). I don't know when this was removed but do know that it's not currently possible in Firefox 128.0.3 on Ubuntu 24.04. Note the lack of an "Add" button in the screenshot below.

![A screenshot of the search engine preferences in Firefox](/assets/images/2024-08-16-firefox-search-engines-before.png)

As per [this Mozilla Bugzilla comment](https://bugzilla.mozilla.org/show_bug.cgi?id=1195005#c21) (from 4 years ago!) the solution appears to be to add `browser.urlbar.update2.engineAliasRefresh` and set it to `true` in Firefox's Advanced Preferences (`about:config`).

![A screenshot of the Firefox configuration option required to allow search engines to be added](/assets/images/2024-08-16-firefox-about-config.png)

With the above option set to `true` I'm now able to add custom search engines again.

![A screenshot of the search engine preferences in Firefox after enabling them to be added](/assets/images/2024-08-16-firefox-search-engines-after.png)

My motivation is to be able to add search engine shortcuts that aren't (as far as I'm aware) possible using the techniques in the [Add or remove a search engine in Firefox docs](https://support.mozilla.org/en-US/kb/add-or-remove-search-engine-firefox). For example I've added a shortcut to search wiki pages in one of our private GitHub repos:

![A screenshot of adding a custom search engine in Firefox](/assets/images/2024-08-16-firefox-add-search-engine.png)

Which allows me to type `@gfrwiki` in the Firefox Address bar in order to search for the pages I want instead of having to navigate to the wiki interface to use the in-page search.

![A screenshot of searching the GFR Wiki custom search engine in Firefox](/assets/images/2024-08-16-firefox-search-in-address-bar.png)