# Restaurant Recommendation System
•	Performed static & steaming recommendation on Yelp dataset based on user location, cuisine and user reviews.
•	Static recommendation was performed using ALS Algorithm and Streaming recommendation was performed using Kafka on user reviews. The user reviews were analysed based on the sentiments and top 5 restaurants were plotted on a map using kibana.


Steps to run Static Part
Log-in into the cluster
Write - $SPARK_HOME/bin/spark-shell --packages com.databricks:spark-csv_2.10:1.5.0
Now copy and paste the program from file StaticRecommendation.scala 

Program will ask for command line input:
Example:
Enter type of Food: Indian
Enter City: Pittsburgh
Enter State: PA
Enter User ID: Fr12lvqUHN6dmMysQ

Based on your search, the top 5 Restaurants will be displayed.

Steps to run Dynamic streaming
1. Start the following servers
	a) Zookeeper
	b) Kafka
	c) Elastic Search
	d) Kibana
2. Run the Kafka Producer(yelpScrapper.py) in PySpark
3. Run the Kafka Consumer(consumer.py) in PySpark
4. Run the Recommender program (recommender.py) in PySpark
5. Open the kibana server in local browser(localhost:5601) for the visualization.


