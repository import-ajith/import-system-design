# Big data ingestion System Design



  
 ![alt text](https://github.com/import-ajith/import-system-design/blob/master/bigdata_ingestion_streaming/bigdata_ingestion_streaming.png)



Comments


		It is common to have “generic” connectors or solutions to offload data from kafka to HDFS,Amazon s3 and Elastic search
	
		Kafka serves two rows,”speed layer” for real time applications ,while having “slow layer” which helps with data ingestions into stores for later analytics.
	
	  Amazon s3,RDBMS,hadoop connect kafka through kafka connect .This data is using for data analytics,reporting ,auditing or even back up
	
		 Kafka as a front to Big Data Ingestion is a common pattern in Big Data to provide an “ingestion buffer” in front of some stores
