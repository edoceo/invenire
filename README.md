# Invenire (In ve nee ray)

A search engine for internal corporate data.

Frequently organizations have knowledge distributed across:

- Email
- Google Drive / Office 356
- Mattermost / Slack / Discord
- Internal Sites / Wikis

And it's hard to find what you know that you know, or used to ... now where was it?

## Index & Search

Create the Content records:

```
curl -X POST "$SERVER/content" \
	--data 'origin=$LINK' \
	--data 'title=' \
	--data 'content=' \
	--data 'type=' \
	--data 'label=' \
```

And then Search:

```
curl "$SERVER/search?q="
```

## Crawlers

Crawlers can be created in whatever language you prefer.
There are some default crawlers provided in `./lib/Crawler`.

```
./bin/crawl.php --origin=$LINK
```


