# DE_Hacker_News_Data_Pipeline

This is guided project from Dataquest.io
The data we will use comes from a Hacker News (HN) API that returns JSON data of the top stories in 2014.
The list of JSON posts is downloaded to a file called hn_stories_2014.json. The JSON file contains a single key stories, which contains a list of stories (posts). Each post has a set of keys, but we will deal only with the following keys:
•	created_at: A timestamp of the story's creation time.
•	created_at_i: A unix epoch timestamp.
•	url: The URL of the story link.
•	objectID: The ID of the story.
•	author: The story's author (username on HN).
•	points: The number of upvotes the story had.
•	title: The headline of the post.
•	num_comments: The number of a comments a post has.
In this project, we will:
-	create file_to_json() which loads the hn_stories_2014.json file into a Python dict and returns the list of stories
-	create filter_stories() that filters popular stories that have more than 50 points, more than 1 comment, and do not begin with Ask HN
-	Create a pipeline.task() function that depends on the filter_stories() and create json_to_csv() function
-	Create extract_titles(), that returns a generator of every Hacker News story title
-	create clean_titles(), will return a generator of clean titles
-	create build_keyword_dictionary(), that returns a dictionary of the word frequency of all the HN
-	finally run the pipeline

