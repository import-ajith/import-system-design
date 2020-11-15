# Bank Streaming System Design

 Requirements

	•	The transaction data already exists in a database
	
	•	Thresholds can be defined by the users
	
	•	Alerts must be sent in real time to the users

  
 ![alt text](https://github.com/import-ajith/import-system-design/blob/master/movie_streaming_design/bank_streaming.png)



Comments


		Bank transactions topics:
	
		•	Kafka Connect source is a great way to expose data from existing database
		•	Change data capture refers to the process or technology for identifying and capturing changes made to a database.
		
		Kafka Stream application:
	
		•	When a user changes their settings ,alert won’t be triggered for past transactions
		
		User threshold topics:
	
		•	It is better to send events to the topic (User 123 enable threshold at $1000 at 12 pm July 12th, 2018)
		•	Than sending the state of the user  (User 123: threshold $1000) if we won’t the information future
