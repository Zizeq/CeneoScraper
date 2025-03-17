# CeneoScraper
https://www.ceneo.pl/84514582#tab-reviews_scroll
## Ceneo scraping algorithm
1. Analysis of the structure of the website.
2. Sending Http request to access first page with opinions.
3. Checking the code of the Http response.
4. Parse the html code of first page with opinions.
5. Extract required data from parsed code.
6. If there are more pages, move to the next page and repeat steps 2-6 for it.
7. Save extracted data.

## Analysis of the structure of the webpage
|Component|Selector|Variable|
|---------|--------|--------|
|opinion ID |data-entry-id | |
|author |user-post__author-name | |
|recommendation |user-post__score  | |
|number of stars |user-post__score-count | |
|list of advantages |review-feature__title | |
|list of disadvantages |review-feature__title | |
|for how many helpful |votes-yes-<post_ID> | |
|for how many unhelpful |votes-no-<post_ID> | |
|publishing date |user-post__published | |
|purchase date | | |