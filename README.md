# CeneoScraper
https://www.ceneo.pl/84514582#tab=reviews
## Ceneo scrapiing algorithm
1. Analysis of the structure of the webpage
2. Sending Http request to access first page with opinions
3. Checking the code of http responce
4. Parse the html code of first age with opinions
5. Extract required data from parsed code
6. If there are more pages, move to the next page and repeat steps 2-6 for it
7. Save extracted data

## Analysis of the structure of the webpage
|Component|Selector|Varriable|
|---------|--------|---------|
|opinion|div.js_product-review|opinion|
|opinion ID|[data-entry-id]|opinion ID|
|author|span.user-post_author-name|author|
|recomendation|span.user-post_author-recomendation|recomendation|
|number of stars|span.user-post__score-count|stars|
|content of opinion|div.user-post__text|content|
|list of advantages|div.review-feature__item--positive|advantages|
|list of disadvantages|div.review-feature__item--negative|disadvantages|
|for how many helpful|button.vote-yes[data-total-vote]|helpful|
|for how many unhelpful|button.vote-no[data-total-vote]|unhelpful|
|publishing date|span.user-post__published > time:nth-child(1)[datetime]|publish date|
|purchase date|span.user-post__published  > time:nth-child(2)[datetime]|purchase date|

