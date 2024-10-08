---
title: 'TweetCoding: Display tweets embedded in coding form for analysis'
date: 2019-04-06T17:00:46+11:00
layout: post
profile: true
aliases: 
  - /2019/04/06/tweetcoding-display-tweets-embedded-in-coding-form-for-analysis/
tags:
  - Internet
  - Social Media
# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  # Caption (optional)
  caption: "TweetCoding screen"
  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point: "Center"
  # Show image only in page previews?
  preview_only: true
---
TweetCoding is a tool for simple coding of tweets. It displays 5 tweets per page using Twitter’s tweet embedding to display each tweet as it looks on the Twitter website on a local web page. It needs internet access to get the tweets from Twitter, but all coding data is stored on your computer, not the internet.

{{< figure src="tweet_coding_screenshot.png" title="Tweet Coding Screen" alt="Shows top of screen with Load New Dataset and Save Coding Data buttons and first two tweets with coding options" >}}

The page has form elements for coding each tweet as yes/no/not coded and a comment field for notes.

The first step is to put the list of tweet-id's for the tweets you want to study into the "Tweet ID editor" section of the form. The page will refresh with the first 5 tweets showing and buttons to move between pages. As you progress the coding is saved locally using browser data storage. The coding data can be exported at any time as a comma delimited (csv) file by using the “Export data” option.

The local browser storage can be reset back to the default Donald Trump example tweet set at any time by pressing "Reset".

This is a open source application that runs locally in your browser and displays embedded tweets so they can be coded as "True", "False", "unknown" and notes recorded against each tweet. To use the app open `index.html` in the `dist` directory. By default a sample dataset of Donald Trump tweets (sourced from https://archive.org/details/trump-tweet-ids) is displayed.

## Instructions from READ.ME file:

To show your own dataset, open the `Tweet ID editor` dropdown and replace the default tweet ids with your own tweet ids - one per line. The `Tweet ID editor` can then be minimised to give more screen space for coding.

Your coding will be saved on your local disk and persists between sessions.

You can use the `reset` button to remove any previous coding.

The coding can be exported to a CSV file by using the `Save Data (CSV)` link.

## Citing

If you use this tool in your research please cite it as

Brenda Moon (2017) tweet-coding 1.0: [![DOI](https://zenodo.org/badge/98805900.svg)](https://zenodo.org/badge/latestdoi/98805900)

## Development

To contribute to the development of this tool you need to have Node.js installed. It is available here: https://nodejs.org/en/download/ (this will also install npm)

I welcome pull requests and reporting of problems via GitHub issues.

### To run in development mode:

```bash
npm install
npm run watch
```

### To build for distribution:

```bash
npm run build:dist
```
