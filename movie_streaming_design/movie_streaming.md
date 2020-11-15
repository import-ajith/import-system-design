# Movie Streaming System Design

 Requirements

 •	Make sure the user can resume the video where they left it off

 •	Build a user profile in real time

 •	Recommend the next show to the user in real time

 •	Store all the data in analytics store
 
 
 
![alt text](https://github.com/import-ajith/import-system-design/blob/master/movie_streaming_design/movie_streaming.png)



Comments

 • Create two kafka topic
       
        • video_position
        • recommendations
        
 •  video_position 
     
      • This topic can have multiple producers
      • should be highly distributed and high volume
      • topic key is "user_id"
    
 •  recommendations
 
     • source data from analytical store for historical training
     • May be low volume topic
     • I would choose "user_id" as key
    
