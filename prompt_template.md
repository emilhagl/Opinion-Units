## Prompt template for generating Opinion Units

Perform aspect-based sentiment analysis for the restaurant review provided as the input.
Return each aspect-sentiment pair with a label and a corresponding excerpt from the text.
Also mark the sentiment of aspects as negative or positive.

Aspect-sentiment pairs should not mix opinions on different aspects. Make sure to include
all aspects. An aspect should be independent and not have to rely on other aspects to be
understood.

If an opinion in the review is about the restaurant or experience in general then label
this aspect as “overall experience”. Opinions not related to the restaurant should not be
included.

**Example input**: I just left Mary’s with my lovely wife. The gorgeous outdoor patio
seating was fantastic with a nice view of the ocean. We came for brunch and were blown
away! We split dozen oysters. They were the best I had in my life! FRESH! Delicious!
The avocado toast was excellent as were the crab cakes. Altogether, we had a great
experience. Almost 5 stars! but the staff could have been a little friendlier and the tables
cleaner.

**Example output**:
[[“Outdoor patio seating”, “The gorgeous outdoor patio seating was fantastic with a nice
view of the ocean”, “positive”],
[“View”, “a nice view of the ocean”, “positive”],
[“Brunch”, “We came for brunch and were blown away”, “positive”],
[“Oysters”, “We split a dozen oysters. They were the best I had in my life! FRESH!
Delicious!”, “positive”],
[“Avocado toast”, “the avocado toast was excellent”, “positive”],
[“Crab cakes”, “the crab cakes were excellent”, “positive”],
[“Overall experience”, “Altogether, we had a great experience. Almost 5 stars!”, “positive”],
[“Staff friendliness”, “the staff could have been a little friendlier”, “negative”],
[“Table cleanliness”, “the tables could have been cleaner”, “negative”]]

**Input**: Review to be processed

**Output**:
