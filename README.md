
# Feed.TXT - A Free Feeds in Plain Text w/ Structured Meta Data


What's Feed.TXT? Let's start with an example from JSON Feed spec:

```json
{
    "version": "https://jsonfeed.org/version/1",
    "title": "My Example Feed",
    "home_page_url": "https://example.org/",
    "feed_url": "https://example.org/feed.json",
    "items": [
        {
            "id": "2",
            "content_text": "This is a second item.",
            "url": "https://example.org/second-item"
        },
        {
            "id": "1",
            "content_html": "<p>Hello, world!</p>",
            "url": "https://example.org/initial-post"
        }
    ]
}
```

Simple, isn't it? Let's try just text:

```
|>>>
 title:          My Example Feed
 home_page_url:  https://example.org/
 feed_url:       https://example.org/feed.txt
 </>
 id:  2
 url: https://example.org/second-item
 ---
 This is a second item.
 </>
 id:  1
 url: https://example.org/initial-post
 ---
 Hello, world!
<<<| 
```

Are you serious, really? Let's try another example from the JSON Feed spec:

```json
{
    "version": "https://jsonfeed.org/version/1",
    "user_comment": "This is a podcast feed. You can add this feed to your podcast client using the following URL: http://therecord.co/feed.json",
    "title": "The Record",
    "home_page_url": "http://therecord.co/",
    "feed_url": "http://therecord.co/feed.json",
    "items": [
        {
            "id": "http://therecord.co/chris-parrish",
            "title": "Special #1 - Chris Parrish",
            "url": "http://therecord.co/chris-parrish",
            "content_text": "Chris has worked at Adobe and as a founder of Rogue Sheep, which won an Apple Design Award for Postage. Chris’s new company is Aged & Distilled with Guy English — which shipped Napkin, a Mac app for visual collaboration. Chris is also the co-host of The Record. He lives on Bainbridge Island, a quick ferry ride from Seattle.",
            "content_html": "Chris has worked at <a href=\"http://adobe.com/\">Adobe</a> and as a founder of Rogue Sheep, which won an Apple Design Award for Postage. Chris’s new company is Aged & Distilled with Guy English — which shipped <a href=\"http://aged-and-distilled.com/napkin/\">Napkin</a>, a Mac app for visual collaboration. Chris is also the co-host of The Record. He lives on <a href=\"http://www.ci.bainbridge-isl.wa.us/\">Bainbridge Island</a>, a quick ferry ride from Seattle.",
            "summary": "Brent interviews Chris Parrish, co-host of The Record and one-half of Aged & Distilled.",
            "date_published": "2014-05-09T14:04:00-07:00",
            "attachments": [
                {
                    "url": "http://therecord.co/downloads/The-Record-sp1e1-ChrisParrish.m4a",
                    "mime_type": "audio/x-m4a",
                    "size_in_bytes": 89970236,
                    "duration_in_seconds": 6629
                }
            ]
        }
    ]
}
```

Yes, the world's 1st podcasting feed in plain text ;-) Let's try:

```
|>>>
 comment: This is a podcast feed. You can add this feed to your podcast client using the following URL: http://therecord.co/feed.json
 title:   The Record
 home_page_url: http://therecord.co/
 feed_url:      http://therecord.co/feed.json
 </>
 id:        http://therecord.co/chris-parrish
 title:     Special #1 - Chris Parrish
 url:       http://therecord.co/chris-parrish
 summary:   Brent interviews Chris Parrish, co-host of The Record and one-half of Aged & Distilled.",
 published: 2014-05-09T14:04:00-07:00
 attachments:
 - url:           http://therecord.co/downloads/The-Record-sp1e1-ChrisParrish.m4a
   mime_type:     audio/x-m4a
   size_in_bytes: 89970236,
   duration_in_seconds: 6629
 ---
 Chris has worked at [Adobe][1] and as a founder of Rogue Sheep, which won an Apple Design Award for Postage. 
 Chris’s new company is Aged & Distilled with Guy English — which shipped [Napkin](2), 
 a Mac app for visual collaboration. Chris is also the co-host of The Record. 
 He lives on [Bainbridge Island][3], a quick ferry ride from Seattle.
 
 [1]: http://adobe.com/
 [2]: http://aged-and-distilled.com/napkin/
 [3]: http://www.ci.bainbridge-isl.wa.us/
<<<|  
```


## Spec(ification) - How does it work?






## License

The Feed.TXT format and conventions are dedicated to the public domain.
Use it as you please with no restrictions whatsoever.

## Questions? Comments?

Send them along to the [wwwmake mailing list/forum](http://groups.google.com/group/wwwmake). Thanks.


<!-- todo: move footer to layouts -->

Brought to you by [Manuscripts](https://github.com/manuscripts) and friends. You might also like [Bib.TXT](http://bibtxt.github.io) ;-).




