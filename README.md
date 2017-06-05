
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









