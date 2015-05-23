# Call Notes - 21 May 2015

Bill, Nick, and Ian had a call of about an hour on 21 May 2015.

## SHINE Interface

- Ian has a local instance of SHINE working, which is indexing WARCs. Currently, running as a single node operation (albeit on a powerful machine), which is running into production bottlenecks.
    + Nick suggested http://www.gnu.org/software/parallel/ - could this run on https://github.com/ukwa/webarchive-discovery/tree/master/warc-indexer
- On Ingesting
    + Nick provided example of book objects - i.e. books are one object (think of it as the cover), each page is an object that's a child of the book - when ingesting, it's not just copying it's also creating derivatives, metadata, etc.
        * Could we do same process for web archives? Mark up things as it comes in? (this might be something we could 'export' to other groups)
    + We also discussed the automatic creation of metadata - i.e. Title fields/HTML fields/etc. to help make it discoverable (a la MARC data for books)
    + Also issue of differences - i.e. Nick crawls YFile every day, how do you stop deduplication? The way WARCs are structured - with unique hash, date stamp in it - simple deduplication would be tricky.
- Bill has been re-writing HistoryCrawler for Mathematica, raising interesting possibilities for markup:
    + NER w/ Semantic entitites (rather than Stanford)
    + linked data
    + ImageIdentify[]
    + Could compile out to C/Java?
- Nick notes that the OLRC technical committee is getting back together, and we could be a pilot project
- We then spoke about posting the SHINE instance online
    + Nick had previously costed out a massive machine - 40 TB storage, 24/32GB of RAM, multiple cores (was it 32?) - at about $16,000 two years ago
        * Could install in York data center for some one-time costs!
        * Both publically-facing and providing info, but also being a research environment for us!

## Other Updates

- Ian has been working with Jimmy Lin (https://github.com/lintool/warcbase) who has given him and some RAs at Waterloo access to a cluster at UMD: using warcbase to extract links, full-text, NER, MALLET, etc. Ideally we'll have a workflow up for some of this back-end stuff soon.
- Nick suggested using GNU Screen to keep shell connections going even if local computer shuts down - http://www.gnu.org/software/screen/

## To Do
 
- Next call is 18 June @ 3pm, Google Hangouts
- Look into parallelizing the warc-indexing process using GNU Parallel (http://www.gnu.org/software/parallel/)
- Look into providing secure access to Nick and Bill from Ian's computer so you can play with Shine (might purchase a cheap $5/month license from <https://forwardhq.com/> for this)
- Ian will harass UW Library at some point about the cluster storage...

## Interim Updates

- Using ngrok to establish link to the local instance of Shine - sent links to rest of project team.
- command is `ngrok http 9000` if running on localhost:9000. Forwardhq ended up breaking everything for some reason.
