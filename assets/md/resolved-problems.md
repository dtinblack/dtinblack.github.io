---
layout: page
title: Resolved Problems
modified: 2022-01-26
---

Over the years Goolge has flagged a number of problems with Jekyll that is used for this blogging site. The following are solutions to the problems:

<b>Problem: Video page indexing issue(s) - 10-February-2022</b>

The blogging site uses embbeded YiouTube videos that were causing the problem. Using the [Inspect the page URL](https://support.google.com/webmasters/answer/9012289?hl=en), then click <b>Test live URL > View tested page > Screenshoot</b> showed that Google could not determinbe the prominent video on the page. The problem that was giving the message was that the video had been blocked by the CORS policy: No'Access-Control-Allow-Origin'header is present on the requested resource.

Searching through [YouTube Embedded Players and Player Parameters](https://developers.google.com/youtube/player_parameters) showed that additional parameters had to be added to the embbeded YouTube call:

```
<iframe width="560" height="315"
src="//www.youtube.com/embed/{particular YouTube video}?enablejsapi=1&origin={url of blogging web site}"
frameborder="0">
</iframe>  

```

to resolve the problem and improve security.
