# scrape-data-from-twitter
A model built on python's tweepy and pandas to scrape data from twitter using twitter API.

This code retrieves tweets from a specified Twitter user, processes the tweet data, and stores it in a Pandas DataFrame for further analysis. Here's a breakdown of what each part of the code does:

1. **Importing Libraries**: The code begins by importing the necessary libraries: `tweepy` for interacting with the Twitter API, `pandas` for data manipulation, and `time` for time-related functions.

2. **Twitter API Authentication**: The code initializes variables `consumer_key`, `consumer_secret`, `access_token`, and `access_token_secret` with the corresponding API keys obtained from the Twitter Developer portal. These keys are used for OAuth1 authentication to access the Twitter API.

3. **Authentication and API Instantiation**: The `tweepy.OAuth1UserHandler()` function is used to authenticate the Twitter API with the provided keys. An `api` object is instantiated using the authenticated `auth` object.

4. **User and Tweet Retrieval**: The code specifies the Twitter user (`username`) from whom to retrieve tweets and the number of tweets to fetch (`no_of_tweets`). It then attempts to retrieve the specified number of tweets using the `api.user_timeline()` method.

5. **Tweet Attributes Extraction**: For each retrieved tweet, the code extracts several attributes such as the tweet's creation date, number of likes, source, and text content. These attributes are stored in a list of lists called `attributes_container`.

6. **DataFrame Creation**: The `attributes_container` is used to create a Pandas DataFrame named `tweets_df`. The column names are specified in the `columns` list, which is passed as an argument when creating the DataFrame.

7. **Exception Handling**: The code is wrapped in a `try-except` block to handle potential exceptions that may occur during tweet retrieval or DataFrame creation. If an exception occurs, the code prints an error message along with the exception details and waits for 3 seconds before continuing.

To follow this code and understand its output in a well-structured format:

- Ensure that you have obtained the necessary API keys from the Twitter Developer portal and replace the empty strings in the `consumer_key`, `consumer_secret`, `access_token`, and `access_token_secret` variables with your actual keys.

- Specify the `username` of the Twitter user from whom you want to retrieve tweets.

- Define the `no_of_tweets` variable to specify the number of tweets you want to fetch.

- Execute the code, and it will retrieve the tweets from the specified user, process the data, and store it in a Pandas DataFrame named `tweets_df`.

- You can then print or analyze the contents of the DataFrame `tweets_df` to see the retrieved tweet data in a structured format, with columns representing different attributes of each tweet.
