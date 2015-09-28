# makeweirdmusic.github.io

[MakeWeirdMusic.com](http://MakeWeirdMusic.com) is an open source website under a [Creative Commons Attribute-NonCommercial-ShareAlike 4.0 International license](http://creativecommons.org/licenses/by-nc-sa/4.0/). The site is run and maintained by [Anthony Garone](http://garone.org). It smells a little funny.

Based on the code quality in this repository, you'll easily guess that I know enough to be dangerous, but am not Mr. Open Source Project Guy. If you'd like to contribute to the site, here's what you should know...

## Artwork

No content will be promoted to master unless there is existing SVG **and** PNG artwork in [our art repository](http://github.com/makeweirdmusic/art).

## Content categories

There are four primary content categories on the site:

1. Discover: Kind of an overview of an artist/band
2. Interview: Obvious
3. Learn: Educational content featuring weird music and/or techniques
4. Share: Performance of some weird music

### Discover

If you're going to contribute to the site, I imagine this will be the section to which you'll contribute. The other ones are a bit more challenging, but certainly not outside the realm of possibility.

I try to answer the following questions about an artist/band:

- Who are we talking about? This should be answered in one paragraph.
- What's weird about this artist? This should be a couple paragraphs featuring techniques regularly used by the artist.
- Why do I know/care about this artist? This is where content is personal and connects with the reader.
- Which songs/albums should the reader listen to first? This can be a list, paragraph, couple paragraphs, etc.

Soundcloud and YouTube embeds are welcome as long as the embed fills the width of the content container.

### Interview

I don't expect you to be contributing interview content to the site, but if you do we'll probably work together on it.

### Learn

This can be a series of one or more videos or written lessons teaching the reader songs of techniques something "weird." The more personal and informative, the better. Please feature a breakdown of chords, time signatures, etc. with musical notation, tablature, and/or PDFs of charts. If you use images, PDFs, whatever, please contribute that content to the [assets repository](http://github.com/makeweirdmusic/assets).

### Share

This should feature a performance or a lecture or something by one or more weird musicians in a way that is compelling to the reader.

## Metadata

Important files containing metadata are:

- [artists.yaml](_data/artists.yaml)
- [authors.yaml](_data/authors.yaml)

### artists.yaml

Look in the file to see how it works, but basically...

```yaml
artist-name:
  name: Human Readable Artist Name
  website: http://url.to.artist.com
  wikipedia: http://en.wikipedia.org/wiki/Artist_Name
  spotify: https://open.spotify.com/artist/artist_id/etc
  itunes: https://itunes.apple.com/us/artist/artist-name/etc
  youtube: https://www.youtube.com/user/artist-user-name
  soundcloud: https://soundcloud.com/artist-name
  google: https://plus.google.com/artist-id
  facebook: https://facebook.com/artist-page
  twitter: https://twitter.com/artist-id
  github: http://github.com/artist-id
```

I don't think I support any other services not listed above. If something comes up, be sure to add a font-awesome icon in the [default.html](_layouts/default.html) &lt;section class="info pane"&gt; element.

### authors.yaml

Site authors get listed here.

```yaml
your-name:
	name: Your Name
```

Again, see other entries for reference.

## Front Matter

In each post document is relevant front matter. Here's [an example](_posts/discover/2015-08-30-steve-vai.markdown):

```yaml
---
layout: post
title:  "Discover Steve Vai"
date:   2015-09-13 19:14:46
artist: steve-vai
author: anthony-garone
image: steve-vai
category: discover
permalink: /discover/steve-vai/
oneliner: Stunt guitarist for Frank Zappa with a solo career spanning over 30 years.
seo_description: Steve Vai is a virtuoso guitarist who has played for Frank Zappa, Whitesnake, Alcatrazz, David Lee Roth, and others.
seo_keywords: Frank Zappa, Whitesnake, David Lee Roth, Alcatrazz, Joe Satriani
front_page: no
techniques:
  - virtuosity
  - composition
  - multiple genres
  - time signatures
---
```

`layout: post` should never change unless you're (for some reason) contributing a new page.

`title` should be the human-readable name of the artist/band (e.g. "Steve Vai") with the category in the relevant place (e.g. "Discover Steve Vai" vs. "Steve Vai Interview").

`date` should be in the format above and can be any recent date.

`artist` is an important field and should match the name of the folder containing the artist's artwork in [our art repository](http://github.com/makeweirdmusic/art) as well as the field in [artists.yaml](_data/artists.yaml).

`author` should match the computer-readable name you put in [authors.yaml](_data/authors.yaml).

`image` should match the name of the artwork file *without the file extension* in the relevant folder in the art repository.

`category` should match the containing folder in [posts](_posts) ("discover", "learn", "share", or "interview").

`permalink` should be "category/artist-name"

`oneliner` is a one-line description of the artist that should fit within one of the colorful boxes in the menu on the front page of the site.

`seo_description` is whatever goes into &lt;meta name="description" /&gt; in the page's &lt;head&gt; element.

`seo_keywords` is whatever goes into &lt;meta name="keywords" /&gt; in the page's &lt;head&gt; element.

`front_page` should either be `yes` or `no` depending on whether it's featured content to be shown on the front page. Unless there's an accompanying video, it shouldn't be on the front page.

`techniques` is a list of weird music techniques employed by the artist in a YAML list. Right now, this isn't used anywhere on the site, but it might be at some point in the future.

## Content

Look at other posts within the category in which you're interested. Model the structure off that. Or don't. Just make the content interesting.

## Warnings

I'm not a Jekyll expert or anything. I haven't set this thing up for several environments yet. There's no "dev" confinguration differing from "prod". You're welcome to help with that if I don't get to it, but a key requirement for me is to be able to do a `git pull` and then `jekyll serve --watch`.

There's tons of room for improvement in this repository. Thanks for your interest!
