# CeneoScraper
https://www.ceneo.pl/84514582#tab-reviews_scroll
## Ceneo scraping algorithm
1. Analysis of the structure of the website.
2. Sending HTTP request to access first page with opinions.
3. Checking the code of the HTTP response.
4. Parse the html code of first page with opinions.
5. Extract required data from parsed code.
6. If there are more pages, move to the next page and repeat steps 2-6 for it.
7. Save extracted data.

## Analysis of the structure of the webpage
|Component|Selector|Variable|
|---------|--------|--------|
|opinion|div.js_product-review:not(user-post--highlight)|opinion|
|opinion ID|[data-entry-id]|opinion_id|
|author|user-post__author-name|author|
|recommendation|span.user-post__author-recomendation > em|recommendation|
|number of stars|span.user-post__score-count|stars|
|content of opinion|div.user-post__text|content|
|list of advantages|div.review-feature__item--positive|pros|
|list of disadvantages|div.review-feature__item--negative|cons|
|for how many helpful|button.vote-yes[data-total-vote]|vote_yes|
|for how many helpful|button.vote-yes > span|vote_yes|
|for how many unhelpful|button.vote-no[data-total-vote]|vote_no|
|for how many unhelpful|button.vote-no > span|vote_no|
|publishing date|span.user-post__published > time.nth-child(1)[datetime]|published|
|purchase date|span.user-post__published > time.nth-child(2)[datetime]|purchased|