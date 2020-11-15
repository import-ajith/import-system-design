# Social media Streaming System Design

 Requirements

	•	Users should be able to post,like and comment
	
	•	Users should see the total number of likes and comments as per post in real time
	
	•	High volume of data is expected on the first day of launch
	
	•	Users should be able to see “tranding” posts

 
 
![alt text](https://github.com/import-ajith/import-system-design/blob/master/movie_streaming_design/socialmedia-streaming-design.png)



Comments

 		Responsibilities are “segregated” hence we can call the model CQRS(Command Query Responsibility Segregation)
	
		Post
		•	Are topics that can have multiple producers
		•	Should be highly distributed if high volume >30 partitions
		•	If I were to choose a key,I would choose “user_id”
		•	We probably want a high retention period of data for this topic
		
	   Like.Comments
		•	Are topics with multiple producers
		•	Should be highly distributed as the volume of data is expected to be much greater
		•	If I were to choose a key, I would choose “post_id”
		
		The data itself in kafka should be formatted as “events”
		•	User_123 created a post_id 456 at 2 pm
		•	User_234 liked post_id 456 at 3 pm
		•	User_123 deleted a post_id 456 at 6 pm
      

