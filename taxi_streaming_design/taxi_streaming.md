# Taxi Streaming System Design

 Requirements

 •	The user should match with a close by driver

 •	The pricing should "surge" if the  number of drivers are low or the number of users is high

 •	All the position data before and during ride should be stored in analytical storage so that cost can be computed accurately.
 
 
![alt text](https://github.com/import-ajith/import-system-design/blob/master/movie_streaming_design/taxi-streaming-design.png)



Comments

 • This design could use common IOT solutions

 • Create three kafka topic
       
        • user_position
        • taxi_position
		• surge_pricing
		
        
 •  user_position &  taxi_position
     
      • All topics can have multiple producers
      • should be highly distributed and high volume
      • topic key is "user_id" and "taxi_id"
    
 •  surge_pricing
 
     • The computation of surge pricing comes from kafka stream application
     • Surge pricing is regional therefore topic may have high volume
     • Other topics such as "weather" and "events" etc can be included in the kafka stream application
    
