# ELXN42 Twitter Discussion

Some ideas:
- could we do text analysis on these tweets; separated by date?
- check it out
- take all the URLs, 1.5 million URLs, and check to see what inclusion in the IA CDX

## Text Analysis
- Similarity: <http://reference.wolfram.com/language/ref/JaccardDissimilarity.html> - used commonly for Twitter
- If this than that - drop tweets with hashtags into Google Spreadsheets
- collected 100,000 election tweets based on hashtags, over a much shorter timeframe
- can share the collection
- similarity/dissimilarity measure - Jaccard
        - astronomical to compare all tweets
        - run 100,000 randomly chosen elements to each other; then run similarity/dissimilarity measures
        - pair of hashtags: what's the similarity WITHIN a hashtag
        - scale it up
        - i.e. #CPC, #NDP, #LPC <- low-hanging fruit

## Day-by-day analysis
- see how hashtags trend over time
    + big themes, etc.
    + NER over time, etc.
- Politics

## Other Analysis
- Client analysis
    + Who's accessing by what?
        * Mobile
        * Desktop
        * Twitterclients
    + Scale of mobile devices affects the kinds of interactions people make in a given setting
- Geographic coverage

## Image Analysis
- image and hashtags?
- do different images use different hashtags
- put all the images together in one directory
- machine learner between text/cartoons/photographs
    + train a machine learner on small datasets, run them through, see what are all the political cartoons/face detection/etc.
- 128,462 images
    + Use ImageMagick to reduce to 400px along the largest direction
    + It'd be smaller
    + Supervised learning, somebody has to do about 1000 photos/cartoons/etc. and drag those into clusters (could be a great RA job)
    + Automatic clustering?
    + (by the summer, Ian's got lots of RA team)

## Questions
- and would that be better than doing day-by-day analysis? [thematic vs day-to-day]

## Next steps
- **Bill** writes up quick notebook, comparing pair of tweets from a given hashtag vs another one
- randomly-chosen tweets across hashtags
- 100 times, 1000 times, 10,000 times
    + and then see how it plays out each time
    + if curve looks pretty level, we know that smaller number is giving us a reasonable effort - keep upping until it converges
- thematic
    + cross-hashtag might need more sampling
- **Ian** gets from Nick the day-by-day Twitter data
    + DAY BY DAY BY DAY (eastern)
    + Entity extraction
    + Change over time
    + Sparklines
    + Could try LDA

## Timeline

